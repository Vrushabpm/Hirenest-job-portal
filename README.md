# 🏢 HireNest — Job Portal

A full-stack Job Portal web application built during a **Java Full Stack Internship**, using **Spring Boot** and **Thymeleaf**. The platform connects **Job Seekers** and **Recruiters** under a single portal with an **Admin** panel for management.

---

## 🚀 Live Demo

> Run locally at: `http://localhost:8080`

---

## 📸 Screenshots

### Homepage
![Homepage](screenshots/home.png)

### Login Page
![Login](screenshots/login.png)

### Recruiter Dashboard
![Recruiter](screenshots/recruiter-home.png)

### Job Seeker Dashboard
![JobSeeker](screenshots/jobseeker-home.png)

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Backend | Spring Boot 3.4 |
| Frontend | Thymeleaf + HTML + CSS |
| Database | MySQL 8.0 |
| ORM | Spring Data JPA + Hibernate |
| Cloud Storage | Cloudinary (image & resume upload) |
| Email Service | Gmail SMTP (OTP verification) |
| Security | AES Encryption for passwords |
| Build Tool | Maven |
| IDE | VS Code |

---

## ✨ Features

### 👤 Job Seeker
- Register with OTP email verification
- Complete profile with photo and resume upload
- Search and browse approved jobs
- Apply for jobs with resume
- View all submitted applications

### 🏢 Recruiter
- Register with OTP email verification
- Post new job listings
- View all applicants for each job
- Manage job postings (edit/delete)

### 🔐 Admin
- Login with secure credentials
- Approve or reject job postings
- Manage all jobs on the platform

---

## ⚙️ Setup & Installation

### Prerequisites
Make sure you have the following installed:
- Java 17
- Maven
- MySQL 8.0
- VS Code (with Java Extension Pack)

### Step 1 — Clone the Repository
```bash
git clone https://github.com/Vrushabpm/Hirenest-job-portal.git
cd Hirenest-job-portal
```

### Step 2 — Create MySQL Database
```sql
CREATE DATABASE jobportal;
```

### Step 3 — Configure application.properties
Create `src/main/resources/application.properties` and add:

```properties
spring.application.name=job-portal
server.port=8080

# Database
spring.datasource.url=jdbc:mysql://localhost:3306/jobportal
spring.datasource.username=root
spring.datasource.password=YOUR_MYSQL_PASSWORD

# JPA
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

# Email
spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=YOUR_GMAIL@gmail.com
spring.mail.password=YOUR_APP_PASSWORD
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.starttls.enable=true

# Admin
portal.admin.email=admin@jobportal.com
portal.admin.password=admin123

# File Upload
spring.servlet.multipart.max-file-size=15MB
spring.servlet.multipart.max-request-size=15MB

# Cloudinary
CLOUDINARY_URL=cloudinary://API_KEY:API_SECRET@CLOUD_NAME
```

### Step 4 — Build the Project
```bash
mvn clean install -DskipTests
```

### Step 5 — Run the Application
```bash
mvn spring-boot:run
```

### Step 6 — Open in Browser
```
http://localhost:8080
```

---

## 🔑 Default Admin Credentials

```
Email    → admin@jobportal.com
Password → admin123
```

---

## 📁 Project Structure

```
src/
├── main/
│   ├── java/com/jsp/job_portal/
│   │   ├── controller/       → MVC Controllers
│   │   ├── dto/              → Entity Classes
│   │   ├── helper/           → AES, Email, Cloudinary
│   │   ├── repository/       → JPA Repositories
│   │   └── service/          → Business Logic
│   └── resources/
│       ├── templates/        → Thymeleaf HTML pages
│       ├── static/           → CSS, JS, Images
│       └── application.properties
└── test/
```

---

## 🔐 Security

- Passwords are encrypted using **AES Encryption**
- OTP based **Email Verification** for registration
- **Session based** authentication for all roles
- Admin, Recruiter and Job Seeker have **separate access controls**

---

## 📦 Dependencies

- Spring Boot Starter Web
- Spring Boot Starter Thymeleaf
- Spring Boot Starter Data JPA
- Spring Boot Starter Mail
- Spring Boot Starter Validation
- MySQL Connector
- Cloudinary SDK
- Lombok
- Spring Boot DevTools

---

## 👨‍💻 Developed By

**Vrushabh P M**
Java Full Stack Internship Project

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
