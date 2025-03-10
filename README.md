# Rails API - Authentication Boilerplate

## 🚀 Overview
This project is a backend API built with **Ruby on Rails** using **Devise** and **JWT authentication**. It provides authentication functionalities such as user signup, login, logout, and password reset.

## 🛠 Tech Stack
- **Ruby on Rails 8**
- **Devise** (User authentication)
- **JWT (JSON Web Token)** for API authentication
- **PostgreSQL** (Database)
- **Rack CORS** (Cross-Origin Resource Sharing)

## 📌 Features
- User authentication (Sign up, Login, Logout)
- JWT-based authentication
- Password recovery (Reset password request and update)
- Protected routes requiring authentication

## 📂 Project Setup

### 1️⃣ Clone the repository
```sh
$ git clone https://github.com/YOUR_USERNAME/YOUR_BACKEND_REPO.git
$ cd YOUR_BACKEND_REPO
2️⃣ Install dependencies
sh
Copier
Modifier
$ bundle install
3️⃣ Set up the database
sh
Copier
Modifier
$ rails db:create db:migrate db:seed
4️⃣ Run the server
sh
Copier
Modifier
$ rails s
🔑 Authentication Endpoints
➤ User Signup
http
Copier
Modifier
POST /users
Request body:
json
Copier
Modifier
{
  "user": {
    "email": "test@example.com",
    "password": "password123",
    "password_confirmation": "password123"
  }
}
➤ User Login
http
Copier
Modifier
POST /users/sign_in
Request body:
json
Copier
Modifier
{
  "user": {
    "email": "test@example.com",
    "password": "password123"
  }
}
Response:
Returns a JWT token in the Authorization header.

➤ User Logout
http
Copier
Modifier
DELETE /users/sign_out
➤ Password Recovery
http
Copier
Modifier
POST /users/password
Request body:
json
Copier
Modifier
{
  "user": {
    "email": "test@example.com"
  }
}


🛠 Further Development
Add email configuration for password recovery
Extend user roles & permissions