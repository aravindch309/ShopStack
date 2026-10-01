🛒 ShopStack

A modern full-stack e-commerce platform built for managing products, shopping carts, orders, customers, and store administration.

Status: 🚧 In Development

✨ Features
Customer

User registration and authentication

Browse products

Search and filter products

Product categories

Product details and reviews

Add products to cart

Update cart quantities

Remove products from cart

Checkout flow

Order history

User profile

Admin

Admin dashboard

Product management

Category management

Order management

User management

Inventory tracking

Sales statistics

Technical

REST API

JWT authentication

Role-based authorization

PostgreSQL database

Responsive UI

API error handling

Automated tests

Docker development environment

🧰 Tech Stack
Frontend

React

Vite

Tailwind CSS

React Router

Axios

Backend

Node.js

Express

PostgreSQL

JWT

bcrypt

Testing

Jest

Supertest

Development

Docker

Git

GitHub Actions

📸 Application
Homepage
┌──────────────────────────────────────────────────────────┐
│ ShopStack     Products  Categories       🔍   🛒  Login │
├──────────────────────────────────────────────────────────┤
│                                                          │
│              Everything you need.                        │
│              All in one place.                            │
│                                                          │
│                 [ Shop Now ]                             │
│                                                          │
├──────────────────────────────────────────────────────────┤
│ Featured Products                                        │
│                                                          │
│  ┌────────┐   ┌────────┐   ┌────────┐   ┌────────┐      │
│  │ Laptop │   │ Headset│   │ Watch  │   │ Camera │      │
│  │ ₹79,999│   │ ₹4,999 │   │ ₹8,999 │   │₹24,999 │      │
│  └────────┘   └────────┘   └────────┘   └────────┘      │
└──────────────────────────────────────────────────────────┘

🚀 Getting Started
1. Clone the repository
git clone https://github.com/example/shopstack.git
cd shopstack

2. Install dependencies
cd server
npm install

cd ../client
npm install

3. Configure environment variables

Create a .env file inside server/.

PORT=5000
DATABASE_URL=postgresql://postgres:password@localhost:5432/shopstack
JWT_SECRET=your_secret_key
NODE_ENV=development


Create a .env file inside client/.

VITE_API_URL=http://localhost:5000/api

4. Start PostgreSQL

Using Docker:

docker compose up -d postgres

5. Seed the database
cd server
npm run seed

6. Start the backend
npm run dev

7. Start the frontend
cd ../client
npm run dev


The application will be available at:

Frontend: http://localhost:5173
Backend:  http://localhost:5000

🔐 Authentication

ShopStack uses JWT-based authentication.

Example login request:

POST /api/auth/login
Content-Type: application/json

{
  "email": "demo@shopstack.dev",
  "password": "password123"
}


Example response:

{
  "user": {
    "id": "user_123",
    "name": "Demo User",
    "email": "demo@shopstack.dev",
    "role": "customer"
  },
  "token": "jwt-token"
}

📡 API
Authentication
Method	Endpoint	Description
POST	/api/auth/register	Register user
POST	/api/auth/login	Login
GET	/api/auth/me	Get current user
Products
Method	Endpoint	Description
GET	/api/products	Get products
GET	/api/products/:id	Get product
POST	/api/products	Create product
PUT	/api/products/:id	Update product
DELETE	/api/products/:id	Delete product
Cart
Method	Endpoint	Description
GET	/api/cart	Get current cart
POST	/api/cart	Add product
PUT	/api/cart/:id	Update quantity
DELETE	/api/cart/:id	Remove item
Orders
Method	Endpoint	Description
POST	/api/orders	Create order
GET	/api/orders	Get user orders
GET	/api/orders/:id	Get order
PUT	/api/orders/:id/status	Update order status
🗄️ Database

Main entities:

User
 │
 ├── Orders
 │
 └── Cart

Product
 │
 ├── Category
 │
 └── OrderItem

Order
 │
 └── OrderItems

User
id
name
email
password
role
createdAt
updatedAt

Product
id
name
description
price
stock
image
categoryId
createdAt
updatedAt

Order
id
userId
totalAmount
status
shippingAddress
createdAt
updatedAt

🧪 Testing

Run backend tests:

cd server
npm test


Run tests with coverage:

npm run test:coverage

🐳 Docker

Start the complete development environment:

docker compose up


Stop containers:

docker compose down

🗺️ Roadmap
Phase 1 — Foundation

 Project structure

 Database setup

 Authentication

 Product API

 Basic product UI

Phase 2 — Shopping

 Shopping cart

 Checkout flow

 Order creation

 Payment integration

 Product reviews

Phase 3 — Administration

 Admin authentication

 Admin dashboard

 Inventory management

 Sales analytics

 User management

Phase 4 — Production

 Image storage

 Email notifications

 Payment gateway

 CI/CD

 Production deployment

🔒 Security

ShopStack follows several basic security practices:

Password hashing with bcrypt

JWT authentication

Protected API routes

Role-based authorization

Input validation

Environment-based secrets

Centralized error handling

Never commit .env files or production secrets.

🤝 Contributing

Fork the repository.

Create a feature branch.

git checkout -b feature/product-reviews


Make your changes.

Run the tests.

npm test


Commit your changes.

git commit -m "feat: add product reviews"


Push your branch.

git push origin feature/product-reviews


Open a pull request.

📄 License

This project is available under the MIT License.

👨‍💻 Author

ShopStack Team

Built as a full-stack e-commerce learning and portfolio project.
