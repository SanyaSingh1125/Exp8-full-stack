![15a46c43-da7f-4b51-bc04-203e4985bd11](https://github.com/user-attachments/assets/585fd68d-b489-4dcd-b659-6e33eed2a7d8)![b3628482-f984-4b44-b5e2-2228ca166177](https://github.com/user-attachments/assets/19084429-6b65-438d-b4b4-dabdbfc2d52c)# Spring Boot Product Management API with JWT Authentication

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
![19608f88-b699-49e6-88fb-ba1c92156fef](https://github.com/user-attachments/assets/42064491-3e53-46f2-8875-00c8b922c2f2)


---

2. Register Admin
![799b3426-c3ba-442b-923c-99e4fde06187](https://github.com/user-attachments/assets/eb21668d-2f2c-41fd-a99f-d4cf67126770)



---

3. Login

Admin Login:
![a0772c5c-e73c-4445-b88c-bee53f7de916](https://github.com/user-attachments/assets/cff5bbb2-ea63-40e6-8f58-d5e28024ce0e)



User Login:
![2d3f37e2-ba2f-4795-92b4-af9b115c7531](https://github.com/user-attachments/assets/be9d28c5-8833-4d66-9216-7334cc5094f5)



---

4. Refresh Token
![e0128b9b-d2cb-4249-a530-f3a514fc7a34](https://github.com/user-attachments/assets/f84463f3-e58a-4572-beae-d5c91fbd5c57)



---
5. Get All Users>
![b3628482-f984-4b44-b5e2-2228ca166177](https://github.com/user-attachments/assets/cb11a1fb-180b-4fa4-bb2e-4bd6dc920c61)



---

6. Get User by ID
![c1417ccf-cfde-498b-9c8f-4d5ea7410f9b](https://github.com/user-attachments/assets/aa2db356-dbf5-48d1-b59d-9dab2808f90f)



---

7. Update User
![35c7500f-56af-46e4-a2e1-38bcc0e823bd](https://github.com/user-attachments/assets/cabf90e6-1599-4f83-9d91-eab1d58f843c)




---

8. Delete User
![b2214f8c-f3b4-4762-9bfc-79c24f7124f0](https://github.com/user-attachments/assets/55e3e8f3-ec07-4720-a133-17ab32a8a1ca)



---

9. Get All Products

<img width="1024" height="658" alt="image" src="https://github.com/user-attachments/assets/5bf927a1-0e3e-490a-8fe7-22b4dd404bab" />


---

10. Get My Products

<img width="1024" height="658" alt="image" src="https://github.com/user-attachments/assets/480f8143-582e-4b7f-9320-ac6b414607da" />


---

11. Get Product by ID
<img width="1024" height="658" alt="image" src="https://github.com/user-attachments/assets/45c0df96-091d-42f1-8297-eeb4b1d2977b" />


---

12. Create Product

<img width="1024" height="658" alt="image" src="https://github.com/user-attachments/assets/4fc4e500-68b2-4b1c-9613-05b617595b12" />


---

13. Update Product

<img width="1024" height="658" alt="image" src="https://github.com/user-attachments/assets/238b26f9-fa7c-4698-952b-e5873144abdc" />

---

14. Delete Product
<img width="1024" height="658" alt="image" src="https://github.com/user-attachments/assets/9b0c6f54-9f9d-4377-beef-bde0d73550f8" />


---

15. Unauthorized Access
<img width="1024" height="591" alt="image" src="https://github.com/user-attachments/assets/2ac51e45-7917-43ac-8bb1-fafa1c44a9a6" />


---

16. Role-based restriction

![15a46c43-da7f-4b51-bc04-203e4985bd11](https://github.com/user-attachments/assets/49720fca-3bb9-4272-afbb-21003bad4b97)


---

User access denied to delete product of Admin:
![4d39f19e-96f6-4ed8-9a68-d9c7ca2c599c](https://github.com/user-attachments/assets/8439d9ec-bedd-4de3-9829-529cf083ec30)


---

User update to the admin product forbidden:
<img width="1024" height="715" alt="image" src="https://github.com/user-attachments/assets/a06a23ce-9061-4426-9346-3f0321a91132" />


---

# Author 
Sanya| 23BCS12970
