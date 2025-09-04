Store API

A RESTful API built with Node.js, Express.js, and MongoDB that manages products with advanced filtering, sorting, field selection, and pagination. This project is a backend service designed for e-commerce–like applications.

###  Features

CRUD Operations: Manage products (create, read, update, delete).
Filtering: Query products by company, featured, or name.
Numeric Filters: Filter products using operators (>, <, =, >=, <=) for fields like price and rating.
Sorting: Sort results by one or multiple fields (e.g., price, name).
Field Selection: Return only specific fields from products.
Pagination: Limit results per page and navigate with page & limit query params.
Error Handling: Centralized error middleware and 404 handling.


###  Tech Stack

•Backend: Node.js (JavaScript runtime)
•Framework: Express.js (REST API creation)
•Database: MongoDB (NoSQL database for storing products)
•ORM: Mongoose (Schema definitions and database interaction)
•Configuration: dotenv (Environment variable management)
•Error Handling: express-async-errors (Async error handling middleware)


###   Project Structure
store-api/
├── controllers/           		# Route controllers (products logic)
│   └── products.js
├── db/                			# MongoDB connection setup
│   └── connect.js
├── middleware/        			# Error and 404 middleware
│   ├── error-handler.js
│   └── not-found.js
├── models/            			# Database schemas
│   └── product.js
├── routes/            			# API route definitions
│   └── products.js
├── products.json      			# Sample dataset
├── populate.js        			# Script to import sample data
├── index.js           			# Server entry point
├── .env               			# Environment variables (Mongo URI, port)
├── package.json
└── README.md




Installation

###   Prerequisites

•Node.js (v16+)
•MongoDB (local or cloud e.g., MongoDB Atlas)
•npm or yarn


###  Setup

### Clone repository
git clone https://github.com/yolcubalsude/Jobs-API.git
cd Jobs-API

### Install dependencies
npm install

 Setup environment variables
 Create a .env file in root with:
 MONGO_URI=your_mongodb_connection_string
 PORT=3000

 Populate DB with sample products
node populate.js

 Run server
npm start


REST API Endpoints

Products
	•	GET /api/v1/products
Get all products. Supports filtering, sorting, field selection, and pagination.
	•	GET /api/v1/products/static
Get a static list of products (for testing/demo purposes).
