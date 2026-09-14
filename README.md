# 📚 Lightbooks — Online Book E-Commerce Platform

<p align="center">
  <img src="https://img.shields.io/badge/Angular-22.0.0-DD0031?style=for-the-badge&logo=angular&logoColor=white" alt="Angular" />
  <img src="https://img.shields.io/badge/Node.js-Express-339933?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/MongoDB-Atlas-47A248?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" />
  <img src="https://img.shields.io/badge/Firebase-Hosting-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Firebase" />
  <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chartdotjs&logoColor=white" alt="Chart.js" />
</p>

---

## 🌐 Live Demo

> 🔗 **Website:** [https://lightbooks-8d487.web.app/homepage](https://lightbooks-8d487.web.app/homepage)

---

## 📖 Project Overview

**Lightbooks** is a comprehensive, full-stack e-commerce web platform designed for purchasing, discovering, and exchanging books (including physical books, e-books, second-hand books, and clearance sales). Built with a modern Client-Server architecture, Lightbooks delivers an instant, highly responsive shopping experience on the storefront alongside a feature-packed Admin Dashboard for total operational control.

- **Course:** Web Development (`253BIE503004`)
- **Team:** Group 04

---

## ✨ Key Features

### 🛒 1. Customer Storefront (Client Application)
* **Interactive Homepage:** Promotional banners, trending best-sellers, featured book collections, and category filters.
* **Diverse Book Catalog:**
  * 📘 **Physical Books:** Wide selection across multiple genres and publishers.
  * 📱 **E-Books:** Digital book formats for immediate access.
  * 🔄 **Second-hand & Clearance (Thanh lí):** Budget-friendly and pre-loved books.
  * ✍️ **Author Profiles:** Dedicated author listing and biography pages.
  * 📰 **News & Blog:** Book reviews, literacy articles, and community posts.
* **Modern Book Details Page:**
  * Clean, Fahasa/Tiki-inspired presentation layout.
  * Real-time stock status, original vs. discounted pricing, and book specifications.
  * Reader ratings and reviews section.
  * Contextual recommendations ("Related Books" & "Same Author").
* **Cart & Seamless Checkout:**
  * Dynamic shopping cart with quantity adjustments and instant price calculation.
  * Streamlined multi-step checkout workflow.
  * Instant order confirmation and status tracking.
* **Personal Account Management:**
  * Secure authentication with JWT and SMS/OTP verification.
  * Profile management and password reset.
  * **Personal Bookshelf:** Track owned, read, and favorite books.
  * **Order History:** Real-time tracking of order statuses.
  * **Reward Points & Achievements:** Gamified loyalty rewards system.
  * Address book manager and social account integrations.
  * Notification center and customer support channel.

---

### 🛡️ 2. Admin Management Portal (`/admin`)
* **Analytics Dashboard:**
  * Real-time revenue metrics, order volumes, and customer growth visualizations powered by **Chart.js**.
  * Period-over-period sales performance tracking.
* **Product Management (Books Catalog):**
  * Full CRUD (Create, Read, Update, Delete) operations for books.
  * Image upload and CDN hosting via **Cloudinary**.
  * Stock levels and pricing management.
* **Order & Return Processing:**
  * End-to-end order workflow management (`Pending`, `Shipping`, `Completed`, `Cancelled`).
  * Inspection and handling of customer return requests.
* **Customer Management:**
  * Complete customer directory with detailed purchase histories and activity logs.
* **Marketing & Promotions:**
  * Coupon and voucher creation, discount percentage configuration, and campaign scheduling.
* **System Settings:**
  * Store configuration and policy management.

---

## 🛠️ Technology Stack

| Layer | Technology | Description |
| :--- | :--- | :--- |
| **Frontend** | **Angular 22** | Single Page Application (SPA), Standalone Components, Reactive Forms |
| | **TypeScript** | Strongly typed codebase for maintainability and scalability |
| | **RxJS** | Reactive state handling and asynchronous data streams |
| | **Chart.js** | Rich and responsive analytics charts on Admin Dashboard |
| | **HTML5 / CSS3** | Modern, mobile-first responsive layout |
| **Backend** | **Node.js & Express 5** | High-performance RESTful API service |
| | **JWT (JSON Web Token)** | Secure stateless user authentication & RBAC |
| | **Bcrypt.js** | Salted hashing for user password security |
| | **Multer & Cloudinary** | Cloud-based media upload and asset management |
| | **Twilio** | SMS verification and OTP delivery |
| **Database** | **MongoDB Atlas** | Fully managed cloud NoSQL document database |
| | **Mongoose 9** | Object Data Modeling (ODM) layer for schema validation |
| **Deployment** | **Firebase Hosting** | Fast and secure global hosting for the client SPA |

---

## 📂 Project Structure

```plaintext
WEB-Ecommerce-Sell-Book---Lightbooks/
├── my-app/                         # Frontend Application (Angular 22)
│   ├── src/
│   │   ├── app/
│   │   │   ├── Components/         # Shared UI components (Header, Footer, Modals, ...)
│   │   │   ├── Pages/              # Route views
│   │   │   │   ├── admin/          # Admin Dashboard & Management modules
│   │   │   │   ├── PersonalAccount/# User account & settings pages
│   │   │   │   ├── books-detail/   # Detailed book view
│   │   │   │   ├── homepage/       # Main landing page
│   │   │   │   ├── cart/           # Cart & checkout
│   │   │   │   └── ...             # Other business views
│   │   │   ├── Services/           # Injectable services (Book, Auth, Notification, ...)
│   │   │   ├── app.routes.ts       # Application routing definition
│   │   │   └── ...
│   │   ├── assets/                 # Static assets, local icons, mock datasets
│   │   └── styles.css              # Global application stylesheets
│   ├── angular.json
│   └── package.json
│
├── my_server/                      # Backend API Server (Node.js & Express)
│   ├── config/                     # Database connection setup (MongoDB)
│   ├── controllers/                # Request handling and business logic
│   ├── models/                     # Mongoose Schemas (User, Product, Order, ...)
│   ├── routes/                     # RESTful API route declarations
│   ├── middleware/                 # Auth tokens and authorization middleware
│   ├── .env                        # Environment configurations (Credentials & Ports)
│   ├── index.js                    # Server entry point
│   └── package.json
│
├── firebase.json                   # Firebase Hosting configuration
└── README.md                       # Project documentation
