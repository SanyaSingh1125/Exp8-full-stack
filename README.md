# Spring Boot Product Management API with JWT Authentication

A secure RESTful API built using Spring Boot that provides product management functionality with JWT-based authentication and role-based authorization.

---

## Features

- JWT Authentication (Access + Refresh Token)
- Role-Based Access Control (ADMIN / USER)
- Product Management (CRUD Operations)
- User Management (Admin / USER)
- Pagination Support
- Global Exception Handling
- H2 In-Memory Database

---

## Tech Stack

- Java
- Spring Boot
- Spring Security
- JWT (JSON Web Token)
- Hibernate / JPA
- H2 Database
- Maven

---

## Authentication Flow

1. User logs in with email & password  
2. Server generates JWT access & refresh token  
3. Client sends token in Authorization header  
4. Server validates token for each request  

---

## Roles & Permissions

| Operation | ADMIN | USER |
|----------|--------|------|
| View Products | Yes | Yes |
| Create Product | Yes | Yes |
| Update Own Product | Yes | Yes |
| Update Any Product | Yes | No |
| Delete Product | Yes | Own Only |
| View All Users | Yes | No |
| Delete Users | Yes | NO |

---

##  API Endpoints

###  Authentication
- `POST /api/user/register`
- `POST /api/user/register-admin`
- `POST /api/user/login`
- `POST /api/user/refresh-token`

###  User APIs
- `GET /api/user/all` (Admin only)
- `GET /api/user/{id}`
- `PUT /api/user/update/{id}`
- `DELETE /api/user/delete/{id}` (Admin only)

###  Product APIs
- `GET /api/product/all`
- `GET /api/product/my-products`
- `GET /api/product/{id}`
- `POST /api/product/register`
- `PUT /api/product/update/{id}`
- `DELETE /api/product/delete/{id}`

---

##  How to Run

1. Clone repository
```bash
git clone https://github.com/your-username/springboot-jwt-product-management-Exp-8
```
2. Open in IDE (IntelliJ)
3. Run application
4. Access APIs via Postman
---
## H2 Database Console

URL:
http://localhost:8080/h2-console

Credentials:
```java
JDBC URL: jdbc:h2:mem:demo
Username: sa
Password: password
```
---
## Output

1. Register User

<img width="577" height="545" alt="register user" src="https://github.com/user-attachments/assets/f6274279-99de-4ae9-ad42-336bd7f1d9bf" />

---

2. Register Admin

<img width="571" height="538" alt="admin registered" src="https://github.com/user-attachments/assets/9d6419c8-645d-4cd2-a49f-434dd36f6b26" />

---

3. Login

Admin Login:

<img width="574" height="531" alt="login admin (token)" src="https://github.com/user-attachments/assets/b29e9b63-b095-4f96-9128-d1c5b983ce21" />

User Login:

<img width="569" height="501" alt="user login" src="https://github.com/user-attachments/assets/d8fae45b-81ce-4bb8-8d27-e67837280542" />

---

4. Refresh Token

<img width="573" height="540" alt="new token generated" src="https://github.com/user-attachments/assets/8f742506-53cb-4667-8633-96abbf041db3" />

---

5. Get All Users

<img width="568" height="538" alt="all users list" src="https://github.com/user-attachments/assets/104bca90-ca05-47d0-a8cc-9df47d2781df" />

---

6. Get User by ID

<img width="574" height="455" alt="get user by id" src="https://github.com/user-attachments/assets/66d46642-d3a3-4b26-932b-9f89cc7da1c1" />

---

7. Update User

<img width="582" height="521" alt="user updated" src="https://github.com/user-attachments/assets/22c52054-80db-4991-b593-967b94ff52e9" />

---

8. Delete User

<img width="568" height="347" alt="delete user" src="https://github.com/user-attachments/assets/ee687ce4-039e-43db-9463-28d16f801987" />

---

9. Get All Products

<img width="565" height="525" alt="all products list" src="https://github.com/user-attachments/assets/8f7c3835-4f24-4ba1-9af4-75919e4a1f07" />

---

10. Get My Products

<img width="569" height="537" alt="get my product" src="https://github.com/user-attachments/assets/47b4b0ff-1d69-4c62-94b4-7282e1b18bf8" />

---

11. Get Product by ID

<img width="567" height="472" alt="get product by id" src="https://github.com/user-attachments/assets/d2c7ac44-df49-4656-9397-579cb976b905" />

---

12. Create Product

<img width="567" height="501" alt="user created product" src="https://github.com/user-attachments/assets/4e710ed5-ce44-46a9-8acd-f3937c2a46d6" />

---

13. Update Product

<img width="557" height="549" alt="product updated" src="https://github.com/user-attachments/assets/a104c430-7558-4faf-a86e-5a7c4f477549" />

---

14. Delete Product

<img width="574" height="364" alt="product deleted " src="https://github.com/user-attachments/assets/60506ef0-8734-47e0-9efc-818ea7532ec6" />

---

15. Unauthorized Access

<img width="579" height="342" alt="unauthorized acces without token" src="https://github.com/user-attachments/assets/1846c98a-2af1-44d7-8623-767df7dcc145" />

---

16. Role-based restriction

<img width="573" height="396" alt="role restriced admin operation getting all users" src="https://github.com/user-attachments/assets/f2e40883-c12b-4ec8-9646-5c8d3d2f689f" />

---

User access denied to delete product of Admin:

<img width="578" height="406" alt="user access denied to delete product" src="https://github.com/user-attachments/assets/ee05a706-7660-43fb-b626-4236f79e05f4" />

---

User update to the admin product forbidden:

<img width="582" height="401" alt="user update to the admin product forbidden" src="https://github.com/user-attachments/assets/986c935d-ddf7-4d26-bab7-7f2043d4b6f3" />

---

# Author 
Prerna| 23BCS80341
