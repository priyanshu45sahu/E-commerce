# MegaStore Backend

Welcome to the MegaStore backend, an eCommerce web application built using the MERN stack (MongoDB, Express, React, Node.js). This backend serves as the foundation for managing products, users, and orders in the MegaStore eCommerce platform.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [API Endpoints](#api-endpoints)

## Features

- User authentication (registration and login)
- Product management (CRUD operations)
- Order processing
- Shopping cart functionality
- RESTful API
- Integration with third-party payment gateways

## Technologies Used

- **Node.js**: JavaScript runtime environment
- **Express**: Web framework for building APIs
- **MongoDB**: Database for storing user and product information
- **Mongoose**: ODM for MongoDB
- **jsonwebtoken**: For user authentication
- **dotenv**: For managing environment variables

# API Endpoints

## Authentication

- **POST** `/api/v1/auth/register` - Register a new user
- **POST** `/api/v1/auth/login` - Authenticate a user and return a token
- **POST** `/api/v1/auth/forgot-password` - Request password reset
- **GET** `/api/v1/auth/test` - Test route (admin only)
- **GET** `/api/v1/auth/user-auth` - Protected route for user authentication
- **GET** `/api/v1/auth/admin-auth` - Protected route for admin authentication
- **PUT** `/api/v1/auth/profile` - Update user profile
- **GET** `/api/v1/auth/orders` - Get orders for authenticated user
- **GET** `/api/v1/auth/all-orders` - Get all orders (admin only)
- **PUT** `/api/v1/auth/order-status/:orderId` - Update order status (admin only)

## Categories

- **POST** `/api/v1/category/create-category` - Create a new category (admin only)
- **PUT** `/api/v1/category/update-category/:id` - Update an existing category (admin only)
- **GET** `/api/v1/category/get-category` - Get all categories
- **GET** `/api/v1/category/single-category/:slug` - Get a single category by slug
- **DELETE** `/api/v1/category/delete-category/:id` - Delete a category by ID (admin only)

## Products

- **POST** `/api/v1/product/create-product` - Create a new product (admin only)
- **PUT** `/api/v1/product/update-product/:pid` - Update an existing product (admin only)
- **GET** `/api/v1/product/get-product` - Get all products
- **GET** `/api/v1/product/get-product/:slug` - Get a single product by slug
- **GET** `/api/v1/product/product-photo/:pid` - Get a product photo by product ID
- **DELETE** `/api/v1/product/delete-product/:pid` - Delete a product by ID (admin only)
- **POST** `/api/v1/product/product-filters` - Filter products
- **GET** `/api/v1/product/product-count` - Get the total count of products
- **GET** `/api/v1/product/product-list/:page` - Get products per page
- **GET** `/api/v1/product/search/:keyword` - Search for products by keyword
- **GET** `/api/v1/product/related-product/:pid/:cid` - Get related products by product ID and category ID
- **GET** `/api/v1/product/product-category/:slug` - Get products by category slug

## Payments

- **GET** `/api/v1/braintree/token` - Get Braintree payment token
- **POST** `/api/v1/braintree/payment` - Process Braintree payment (user must be authenticated)

## Root Endpoint

- **GET** `/` - Welcome message for the eCommerce app
