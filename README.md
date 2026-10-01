🛒 ShopStack
Modern e-commerce, built for the web.

ShopStack is a full-stack e-commerce platform where users can discover products, manage their cart, place orders, and track purchases — while store admins can manage products, inventory, customers, and orders from a dedicated dashboard.

<p align="center"> <strong>React</strong> · <strong>Node.js</strong> · <strong>Express</strong> · <strong>PostgreSQL</strong> </p> <p align="center"> <a href="#-features">Features</a> • <a href="#-screenshots">Screenshots</a> • <a href="#-tech-stack">Tech Stack</a> • <a href="#-getting-started">Getting Started</a> • <a href="#-roadmap">Roadmap</a> </p>
✨ Overview

ShopStack was built to explore how a real-world e-commerce application works from end to end.

The project covers everything from browsing products and managing a shopping cart to authentication, order processing, inventory management, and administration.

                    SHOPSTACK
                        │
          ┌─────────────┴─────────────┐
          │                           │
       CUSTOMER                     ADMIN
          │                           │
    ┌─────┴─────┐             ┌───────┴───────┐
    │           │             │               │
 Products     Cart        Products         Orders
    │           │             │               │
    └─────┬─────┘             └───────┬───────┘
          │                           │
          └───────────┬───────────────┘
                      │
                 REST API
                      │
                 PostgreSQL

🚀 Features
🛍️ Shopping

Browse products

Search and filter products

View detailed product information

Add products to cart

Update quantities

Remove items

Calculate cart totals

Responsive shopping experience

👤 Authentication

User registration

Secure login

JWT-based authentication

Protected routes

Role-based authorization

Customer and admin accounts

📦 Orders

Checkout workflow

Create orders

View order history

View individual order details

Track order status

Server-side order validation

🛠️ Admin Dashboard

Product management

Inventory management

Order management

Customer management

Sales overview

Dashboard statistics

📸 Screenshots

Screenshots will be added as the UI is completed.

Home
┌─────────────────────────────────────────────────────┐
│  🛒 ShopStack     Shop    Categories    Search  🛍️ │
├─────────────────────────────────────────────────────┤
│                                                     │
│       Shop smarter.                                 │
│       Live better.                                  │
│                                                     │
│       Discover products you'll love.                │
│                                                     │
│              [ Explore Products ]                   │
│                                                     │
└─────────────────────────────────────────────────────┘

Product Catalog
┌─────────────────────────────────────────────────────┐
│ Products                              🔍 Search... │
├──────────────┬──────────────────────────────────────┤
│ Categories   │                                      │
│              │   ┌──────┐ ┌──────┐ ┌──────┐       │
│ Electronics  │   │      │ │      │ │      │       │
│ Fashion      │   │ 📱   │ │ 💻   │ │ 🎧   │       │
│ Home         │   │      │ │      │ │      │       │
│ Accessories  │   └──────┘ └──────┘ └──────┘       │
│              │                                      │
└──────────────┴──────────────────────────────────────┘

Admin Dashboard
┌────────────┬────────────────────────────────────────┐
│ ShopStack  │  Dashboard                             │
│            │                                        │
│ Dashboard  │  Revenue       Orders      Customers  │
│ Products   │  ₹1.24L        248         1,842      │
│ Orders     │                                        │
│ Users      │  ───────── Sales Overview ─────────   │
│            │                                        │
│ Settings   │       ╱╲      ╱╲                      │
│            │   ╀──╯  ╰────╯  ╰──                  │
└────────────┴────────────────────────────────────────┘

🧰 Tech Stack
Layer	Technology
Frontend	React + Vite
Styling	Tailwind CSS
Routing	React Router
API	Node.js + Express
Database	PostgreSQL
Authentication	JWT + bcrypt
HTTP Client	Axios
Testing	Jest + Supertest
Containers	Docker
Version Control	Git
🏗️ Project Structure
shopstack/
│
├── client/                 # Customer storefront
│   ├── components/
│   ├── pages/
│   ├── context/
│   ├── hooks/
│   └── services/
│
├── server/                 # REST API
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   └── utils/
│
├── admin/                  # Admin dashboard
│   ├── components/
│   └── pages/
│
├── docs/                   # Project documentation
│
├── docker-compose.yml
├── .env.example
└── README.md

🔐 Authentication Flow

ShopStack uses JWT authentication.

User
 │
 │ Login
 ▼
API
 │
 ├── Validate credentials
 │
 ├── Verify password
 │
 └── Generate JWT
          │
          ▼
       Client
          │
          ▼
   Protected Requests
          │
          ▼
    Auth Middleware
          │
          ▼
       API Route


Passwords are never stored in plain text and protected routes require valid authentication.

📡 API
Authentication
POST /api/auth/register
POST /api/auth/login
GET  /api/auth/me

Products
GET    /api/products
GET    /api/products/:id
POST   /api/products
PUT    /api/products/:id
DELETE /api/products/:id

Cart
GET    /api/cart
POST   /api/cart
PUT    /api/cart/:id
DELETE /api/cart/:id

Orders
POST /api/orders
GET  /api/orders
GET  /api/orders/:id
PUT  /api/orders/:id/status

⚡ Getting Started
Prerequisites

Make sure you have installed:

Node.js 18+

npm

PostgreSQL 15+

Git

Docker (optional)

1. Clone
git clone https://github.com/example/shopstack.git

cd shopstack

2. Install dependencies
cd server
npm install

cd ../client
npm install

cd ../admin
npm install

3. Configure environment

Create .env files using the provided examples.

cp server/.env.example server/.env


Example:

PORT=5000
DATABASE_URL=postgresql://postgres:password@localhost:5432/shopstack
JWT_SECRET=your_secret_key

4. Start the backend
cd server
npm run dev

5. Start the frontend

In another terminal:

cd client
npm run dev

6. Open the application
Frontend → http://localhost:5173
API      → http://localhost:5000

🐳 Run with Docker

Prefer Docker?

docker compose up


To stop the containers:

docker compose down

🧪 Testing

Run the backend test suite:

cd server

npm test


Run with coverage:

npm run test:coverage


Current test areas include:

Authentication

Product API

Cart operations

Order creation

Authorization

🗺️ Roadmap
✅ Completed

 Project setup

 Database architecture

 User authentication

 Product API

 Product catalog

 Shopping cart

 Order creation

 Order history

🚧 In Progress

 Admin dashboard

 Inventory management

 Product reviews

 Improved analytics

🔮 Planned

 Payment integration

 Email notifications

 Wishlist

 Discount / coupon system

 Product recommendations

 Image optimization

 CI/CD pipeline

 Production deployment

🔒 Security

ShopStack includes:

Password hashing with bcrypt

JWT authentication

Protected API endpoints

Role-based authorization

Input validation

Environment-based configuration

Centralized API error handling

Never commit .env files or production secrets to the repository.

🤝 Contributing

Contributions are welcome.

# Create a branch
git checkout -b feature/product-reviews

# Make your changes
# Run tests
npm test

# Commit
git commit -m "feat: add product reviews"

# Push
git push origin feature/product-reviews


Then open a pull request.

📌 Project Status
Frontend       ███████████████░░░  80%
Backend        █████████████████░  90%
Authentication ██████████████████ 100%
Cart           ██████████████████ 100%
Orders         ████████████████░░  85%
Admin          ██████████░░░░░░░░  55%
Testing        ████████████░░░░░░  65%


ShopStack is currently under active development.

📄 License

This project is licensed under the MIT License.

<p align="center"> Built with ❤️ using React, Node.js & PostgreSQL </p>
