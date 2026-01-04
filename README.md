# IBM-INTERNSHIP-DAY-4-NM
# 📚 Library Management System (Node.js + MongoDB)

A simple **Library Management System REST API** built using **Node.js, Express, and MongoDB (Mongoose)**.
This project supports basic **CRUD operations** for managing books in a library.

## 🚀 Features

* Add multiple books at once
* View all books
* Filter books by category
* View books published after 2015
* Update available copies of a book
* Change book category
* Delete a book only when copies are zero

## 🛠️ Technologies Used

* **Node.js**
* **Express.js**
* **MongoDB**
* **Mongoose**

## 📂 Project Structure

├── app.js           # Main server file
├── db.js            # MongoDB connection
├── bookmodel.js     # Book schema and model
├── package.json
├── package-lock.json

## ⚙️ Installation & Setup

1. **Clone the repository**
   
git clone https://github.com/your-username/library-management-system.git


3. **Navigate to the project folder**

cd library-management-system


3. **Install dependencies**

npm install


4. **Start MongoDB**
   Make sure MongoDB is running on:

mongodb://127.0.0.1:27017/libraryDB

5. **Run the server**

node app.js

Server will run on:

http://localhost:3000

## 📌 API Endpoints

### ➕ Add Books


POST /addBooks

### 📖 Get All Books

GET /books

### 📚 Get Books by Category

GET /books/category/:category

### 📅 Get Books Published After 2015

GET /books/year/after2015

### 🔄 Update Available Copies

PUT /books/updateCopies/:id

**Body:**

json
{
  "change": 2
}

### 🏷️ Change Book Category

PUT /books/changeCategory/:id

**Body:**
json
{
  "category": "AI"
}

### ❌ Delete Book (Only if copies = 0)

DELETE /books/delete/:id

## ⚠️ Important Notes

* Books **cannot be deleted** if `availableCopies > 0`
* Negative stock is **not allowed**
* Uses **Express JSON middleware**

## 🎯 Future Enhancements

* User authentication
* Borrow & return books
* Pagination & search
* Frontend integration

## 👩‍💻 Author

**Suchithra Sambareddy**
AI & DS Student
