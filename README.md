# 🧵✂️ **Tailor Management System (TailorApp)**

<p align="center">
  <img src="https://img.shields.io/badge/Spring%20Boot-4.0.1-brightgreen?style=for-the-badge">
  <img src="https://img.shields.io/badge/PostgreSQL-Database-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Thymeleaf-Frontend-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/Spring%20Security-Enabled-red?style=for-the-badge">
  <img src="https://img.shields.io/badge/Status-Stable-brightgreen?style=for-the-badge">
</p>

A **secure Tailor Shop Management Application** built with **Spring Boot**, **PostgreSQL**, and **Thymeleaf**, designed specifically for shop owners to manage customers and their measurements efficiently.

---

# 🌐 **Application Overview**

TailorApp is a role-based web application where:

* Only the **Shop Owner** can log in
* Owner can manage customers
* Each customer can have **multiple measurements**
* Measurements are stored with **date tracking**
* Secure authentication ensures protected access

This project simulates a real-world tailoring shop workflow.

---

# 🔐 **Authentication & Authorization**

✔ Secure Login System (Spring Security)
✔ Role-Based Access Control
✔ Protected Routes
✔ Owner-only dashboard access
✔ Session-based authentication

---

# 👨‍💼 **Owner Dashboard Features**

### 🧑 Customer Management

* ➕ Add Customer
* 📄 View All Customers
* ✏️ Update Customer Details
* 🗑 Delete Customer

---

### 📏 Measurements Management

* ➕ Add Measurement (with date)
* 📄 View Measurements per Customer
* ✏️ Update Measurement
* 🗑 Delete Measurement
* 🔗 One Customer → Multiple Measurements (One-to-Many relationship)

---

# 🛠️ **Tech Stack**

| Layer    | Technology                  |
| -------- | --------------------------- |
| Backend  | Spring Boot (Java 17+)      |
| Security | Spring Security             |
| Frontend | Thymeleaf + CSS             |
| Database | PostgreSQL                  |
| ORM      | Spring Data JPA / Hibernate |
| IDE      | STS / IntelliJ IDEA         |

---

# 🗃️ **Database Design**

### 🧑 Customer Table

* id (Primary Key)
* name
* phone
* address
* created_date

### 📏 Measurement Table

* id (Primary Key)
* measurement_date
* shirt_length
* chest
* sleeve
* shoulder
* customer_id (Foreign Key)

🔗 **Relationship:**
One Customer → Many Measurements

---

# 🗄️ **Database Setup (PostgreSQL)**

### 1️⃣ Create Database

```sql
CREATE DATABASE tailorapp;
```

### 2️⃣ Configure Database Connection

Update `application.properties`:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/tailorapp
spring.datasource.username=postgres
spring.datasource.password=your_pg_password
spring.jpa.hibernate.ddl-auto=update
```

### 3️⃣ Add Owner Login (Example)

```sql
INSERT INTO users (username, password, role)
VALUES ('owner', 'encoded_password_here', 'ROLE_OWNER');
```

---

# 🚀 **How to Run the Application**

1. Clone the repository
2. Open in **STS / IntelliJ**
3. Ensure PostgreSQL is running
4. Run as **Spring Boot Application**
5. Access:

```
Login: http://localhost:8080/login
Dashboard: http://localhost:8080/dashboard
```

---

# 📁 **Project Structure**

```
TailorApp/
│
├── src/main/java/...            # Controllers, Services, Entities
├── src/main/resources/templates # Thymeleaf HTML Pages
├── src/main/resources/static    # CSS
├── application.properties
└── README.md
```

---

# ✅ **Feature Matrix**

| Feature                  | Status |
| ------------------------ | ------ |
| Secure Login System      | ✅      |
| Role-Based Access        | ✅      |
| Customer CRUD            | ✅      |
| Measurement CRUD         | ✅      |
| One-to-Many Relationship | ✅      |
| Date Tracking            | ✅      |
| Route Protection         | ✅      |

---

# 🌱 **Future Enhancements**

* 📊 Order tracking system
* 🧾 Invoice generation
* 📅 Delivery date reminder
* 📱 Responsive UI improvements
* 📈 Analytics dashboard

---

# 👨‍💻 **Author**

Your Name Here

---

# 📄 **License**

This project is built for **educational and demonstration purposes**.

---
