# Todo Backend API Documentation

This document provides a comprehensive overview of all available API endpoints in the Todo Backend application.

## Table of Contents
1. [User Management](#user-management)
2. [Todo Management](#todo-management)
3. [Admin Management](#admin-management)

## User Management

### User Signup
![User Signup](images/userSignup1.png)
![User Signup Response](images/userSignup2.png)
- **Endpoint**: `/api/v1/user/signup`
- **Method**: POST
- **Description**: Creates a new user account
- **Request Body**: Email, password, and other user details
- **Response**: Returns user ID and a success message

### User Signin
![User Signin](images/userSignin1.png)
![User Signin Response](images/userSignin2.png)
- **Endpoint**: `/api/v1/user/signin`
- **Method**: POST
- **Description**: Authenticates a user and returns a JWT token
- **Request Body**: Email and password
- **Response**: Returns JWT token and user details

### User Verify OTP
![User Verify OTP](images/userVerifyOTP1.png)
![User Verify OTP Response](images/userVerifyOTP2.png)
- **Endpoint**: `/api/v1/user/verify-otp`
- **Method**: POST
- **Description**: Verifies the OTP sent to user's email
- **Request Body**: Email and OTP
- **Response**: Returns verification status

### User Resend OTP
![User Resend OTP](images/userResendOTP1.png)
![User Resend OTP Response](images/userResendOTP2.png)
- **Endpoint**: `/api/v1/user/resend-otp`
- **Method**: POST
- **Description**: Resends OTP to user's email
- **Request Body**: Email
- **Response**: Returns success message

### Get User Info
![Get User Info](images/userGetInfo1.png)
![Get User Info Response](images/userGetInfo2.png)
- **Endpoint**: `/api/v1/user/info`
- **Method**: GET
- **Description**: Retrieves user information
- **Headers**: Requires JWT token
- **Response**: Returns user details

## Todo Management

### Add Todo
![Add Todo](images/todoAdd1.png)
![Add Todo Response](images/todoAdd2.png)
- **Endpoint**: `/api/v1/todo`
- **Method**: POST
- **Description**: Creates a new todo item
- **Headers**: Requires JWT token
- **Request Body**: Todo title, description, and other details
- **Response**: Returns created todo details

### Update Todo
![Update Todo](images/todoUpdate1.png)
![Update Todo Response](images/todoUpdate2.png)
- **Endpoint**: `/api/v1/todo/{id}`
- **Method**: PUT
- **Description**: Updates an existing todo item
- **Headers**: Requires JWT token
- **Request Body**: Updated todo details
- **Response**: Returns updated todo details

### Get All Todos
![Get All Todos](images/todoGetAll.png)
- **Endpoint**: `/api/v1/todo`
- **Method**: GET
- **Description**: Retrieves all todo items for the authenticated user
- **Headers**: Requires JWT token
- **Response**: Returns list of todos

### Delete Todo
![Delete Todo](images/todoDelete.png)
- **Endpoint**: `/api/v1/todo/{id}`
- **Method**: DELETE
- **Description**: Deletes a todo item
- **Headers**: Requires JWT token
- **Response**: Returns success message

## Admin Management

### Admin Add User
![Admin Add User](images/adminAddUser1.png)
![Admin Add User Response](images/adminAddUser2.png)
- **Endpoint**: `/api/v1/admin/user`
- **Method**: POST
- **Description**: Creates a new user (admin only)
- **Headers**: Requires admin JWT token
- **Request Body**: User details
- **Response**: Returns created user details

### Admin Update User
![Admin Update User](images/adminUpdateUser1.png)
![Admin Update User Response](images/adminUpdateUser2.png)
- **Endpoint**: `/api/v1/admin/user/{id}`
- **Method**: PUT
- **Description**: Updates user details (admin only)
- **Headers**: Requires admin JWT token
- **Request Body**: Updated user details
- **Response**: Returns updated user details

### Admin Delete User
![Admin Delete User](images/adminDeleteUser.png)
- **Endpoint**: `/api/v1/admin/user/{id}`
- **Method**: DELETE
- **Description**: Deletes a user (admin only)
- **Headers**: Requires admin JWT token
- **Response**: Returns success message
