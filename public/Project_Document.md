# 📘 E-Commerce Backend — Technical Documentation

---

## 📌 Introduction

This project is a backend REST API for an e-commerce product catalog. It allows users to perform CRUD (Create, Read, Update, Delete) operations on products using Node.js, Express.js, and MongoDB.

---

## 🎯 Objectives

- Build a scalable backend system
- Implement RESTful APIs
- Manage product data efficiently
- Learn MongoDB integration using Mongoose

---

## 🏗️ System Architecture

The system follows a **3-layer architecture**:

1. **Presentation Layer**
   - API endpoints (routes)

2. **Application Layer**
   - Business logic (controllers - inside routes)

3. **Data Layer**
   - MongoDB database (via Mongoose models)

---

## 📁 Modules Description

### 1. Server Module (`server.js`)
- Initializes Express app
- Connects to MongoDB
- Uses middleware (JSON parsing)
- Defines base routes

---

### 2. Product Model (`models/product.js`)
Defines schema using Mongoose:

- name (String, required)
- description (String)
- price (Number, required)
- category (String)
- stock (Number, default: 0)
- timestamps enabled

---

### 3. Routes Module (`routes/productRoutes.js`)
Handles API requests:

- GET → Fetch products
- POST → Add product
- PUT → Update product
- DELETE → Remove product

---

## 🔄 Data Flow

1. Client sends HTTP request
2. Route receives request
3. Logic processes data
4. Model interacts with database
5. Response sent back to client

---

## 🔐 Environment Configuration

Uses `.env` file:


MONGO_URI=mongodb://localhost:27017/ecommerce
PORT=5000

---

## ⚙️ API Working

### Example Flow: Add Product

1. Client sends POST request
2. Server validates input
3. Mongoose saves data
4. MongoDB stores document
5. Response returned

---

## 📊 Database Design

Collection: `products`

Each document contains:
- _id (auto-generated)
- name
- description
- price
- category
- stock
- createdAt
- updatedAt

---

## 🧪 Testing Strategy

- Tested using Postman
- Verified all CRUD operations
- Checked error handling

---

## ⚠️ Limitations

- No authentication system
- No user roles (admin/customer)
- No image upload support

---
