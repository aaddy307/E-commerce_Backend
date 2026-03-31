# 🛒 E-Commerce Backend — Product Catalog

A simple e-commerce backend REST API built with Node.js, Express.js, and MongoDB for managing a product catalog.

---

## 🛠️ Tech Stack

- **Node.js** — Runtime environment
- **Express.js** — Web framework
- **MongoDB** — NoSQL Database
- **Mongoose** — MongoDB object modeling
- **dotenv** — Environment variable management

---

## 📁 Project Structure

ecommerce-backend/
├── models/
│   └── product.js
├── routes/
│   └── productRoutes.js
├── .env
├── .gitignore
├── server.js
└── package.json


---

## ⚙️ Installation & Setup

### 1. Clone the repository
git clone https://github.com/aaddy307/E-commerce_Backend.git
cd ecommerce-backend

### 2. Install dependencies
npm install

### 3. Create `.env` file
MONGO_URI=mongodb://localhost:27017/ecommerce

### 4. Start the server
node server.js

Server will run on: `http://localhost:5000`

---

## 📦 Product Model

| Field       | Type   | Required | Default |
|-------------|--------|----------|---------|
| name        | String | ✅ Yes   | —       |
| description | String | ❌ No    | —       |
| price       | Number | ✅ Yes   | —       |
| category    | String | ❌ No    | —       |
| stock       | Number | ❌ No    | 0       |
| createdAt   | Date   | Auto     | —       |
| updatedAt   | Date   | Auto     | —       |

---

## 🔗 API Endpoints

Base URL: `http://localhost:5000/api/products`

### Get All Products
GET /api/products

**Response:**
json
[
  {
    "_id": "64abc123...",
    "name": "Nike Shoes",
    "price": 2999,
    "category": "Footwear",
    "stock": 50
  }
]


---

### Get Single Product
GET /api/products/:id

**Response:**
json
{
  "_id": "64abc123...",
  "name": "Nike Shoes",
  "description": "Comfortable running shoes",
  "price": 2999,
  "category": "Footwear",
  "stock": 50
}


---

### Add New Product
POST /api/products

**Request Body:**
json
{
  "name": "Nike Shoes",
  "description": "Comfortable running shoes",
  "price": 2999,
  "category": "Footwear",
  "stock": 50
}


**Response:**
json
{
  "_id": "64abc123...",
  "name": "Nike Shoes",
  "price": 2999,
  "createdAt": "2026-03-31T10:00:00.000Z"
}


---

### Update Product
PUT /api/products/:id

**Request Body:**
json
{
  "price": 3499,
  "stock": 30
}


**Response:**
json
{
  "_id": "64abc123...",
  "name": "Nike Shoes",
  "price": 3499,
  "stock": 30,
  "updatedAt": "2026-03-31T12:00:00.000Z"
}


---

### Delete Product
DELETE /api/products/:id

**Response:**
json
{
  "message": "Product deleted"
}


---

## 🧪 Testing the API

You can test the API using:
- [Postman](https://www.postman.com/) — Recommended
- Thunder Client — VS Code Extension
- curl — Terminal

### Example curl command:
bash
curl -X POST http://localhost:5000/api/products \
-H "Content-Type: application/json" \
-d '{"name": "Nike Shoes", "price": 2999, "category": "Footwear", "stock": 50}'


---

## ❌ Common Errors

| Error | Reason | Fix |
|-------|--------|-----|
| `Cannot POST /api/products` | Server not running | Run `node server.js` |
| `product validation failed` | Missing required fields | Include `name` and `price` |
| `MongooseServerSelectionError` | MongoDB not connected | Check `.env` MONGO_URI |
| `Cast to ObjectId failed` | Invalid product ID | Use correct MongoDB `_id` |

---

## 👨‍💻 Author

- **Name:** Your Name
- **College:** Your College Name
- **Project:** E-Commerce Backend — College Project

---

## 📄 License

This project is for educational purposes only.
```

---

## How to use it:

1. Create a file named **`README.md`** in your project root
2. Paste the above content
3. Replace **Your Name** and **Your College Name** at the bottom

Your final project structure will look like:
```
ecommerce-backend/
├── models/
├── routes/
├── .env
├── .gitignore
├── README.md   ← here
└── server.js