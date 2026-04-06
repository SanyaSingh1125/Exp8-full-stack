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
![19608f88-b699-49e6-88fb-ba1c92156fef](https://github.com/user-attachments/assets/b34f11d6-c925-4142-a3b9-85152729461e)


---

2. Register Admin
![799b3426-c3ba-442b-923c-99e4fde06187](https://github.com/user-attachments/assets/20303078-338f-4b17-ada9-54e8ba2df8d2)


---

3. Login

Admin Login:

![a0772c5c-e73c-4445-b88c-bee53f7de916](https://github.com/user-attachments/assets/424be619-ed54-4002-94aa-85b713cba4ee)


User Login:

![2d3f37e2-ba2f-4795-92b4-af9b115c7531](https://github.com/user-attachments/assets/0ddc0b9e-e018-4b2e-b4ae-614444850d0a)


---

4. Refresh Token

![e0128b9b-d2cb-4249-a530-f3a514fc7a34](https://github.com/user-attachments/assets/3ecefca1-22d2-49dc-84df-35282f6a004a)


---

5. Get All Users>

![b3628482-f984-4b44-b5e2-2228ca166177](https://github.com/user-attachments/assets/6803e89e-7ed4-429b-9987-eda722d0ddb2)

---

6. Get User by ID

![a4ba206a-4c17-4ec0-bd4d-1c0464d347ea](https://github.com/user-attachments/assets/1e87bcb1-1dc7-4afc-8b12-f313d0fb4088)


---

7. Update User

![a50d58b1-8abd-4a2f-8962-ebe8fac07351](https://github.com/user-attachments/assets/6e1345f9-0163-4eac-b7bb-0efe1e548501)


---

8. Delete User

![f3718a61-a222-4931-9a44-4d8ca6523b06](https://github.com/user-attachments/assets/abd61685-229f-4cb1-96a0-9a4f2772d0e4)

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
Sanya| 23BCS12970
