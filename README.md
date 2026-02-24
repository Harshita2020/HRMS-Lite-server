# HRMS Lite - Backend (Express API)

## 📌 Overview

This is the backend service for the HRMS Lite project.

It is a simple REST API built using **Node.js** and **Express** that
manages employee records in memory (no database yet).

The goal of this backend is to strengthen core backend fundamentals
before integrating a real database like MongoDB.

------------------------------------------------------------------------

## 🛠 Tech Stack

-   Node.js
-   Express
-   Nodemon (development)
-   REST API architecture

------------------------------------------------------------------------

## 🚀 Features

### ✅ GET /employees

Returns all employees.

### ✅ GET /employees/:id

Returns a single employee by ID. - Returns 404 if employee does not
exist.

### ✅ POST /employee

Adds a new employee. - Returns success response.

### ✅ PUT /employees/:id

Updates an employee. - Immutable update using object spread. - Protects
`id` from being overwritten. - Returns updated employee. - Returns 404
if employee not found.

### ✅ DELETE /employees/:id

Deletes an employee by ID. - Returns 404 if employee not found.

------------------------------------------------------------------------

## 🧠 Implementation Highlights

-   Uses `findIndex()` for safe array updates.
-   Uses immutable object updates (`{ ...old, ...req.body }`).
-   Preserves original `id` even if client attempts to modify it.
-   Proper HTTP status codes for error handling.

------------------------------------------------------------------------

## 📦 Installation

``` bash
npm install
```

------------------------------------------------------------------------

## 🧪 Development Mode (with Nodemon)

``` bash
npm run dev
```

Nodemon automatically restarts the server on file changes.

------------------------------------------------------------------------

## 🚀 Production Mode

``` bash
npm start
```

------------------------------------------------------------------------

## 📍 Server Runs On

    http://localhost:3000

------------------------------------------------------------------------

## 🔮 Future Improvements

-   Integrate MongoDB with Mongoose
-   Add request validation (Joi / Zod)
-   Add structured logging
-   Add environment configuration (.env)
-   Add authentication layer
-   Add unit tests

------------------------------------------------------------------------

## 📚 Learning Focus

This backend focuses on:

-   REST principles
-   Immutable update patterns
-   Safe array manipulation
-   API design fundamentals
-   Clean project setup (git + gitignore + dev scripts)

------------------------------------------------------------------------

Built as part of ongoing full-stack development practice.
