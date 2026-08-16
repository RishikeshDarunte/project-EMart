# 🛒 E-Mart

E-Mart is a full-stack e-commerce web application built as a CDAC major project. It lets customers browse products, manage their cart and wishlist, check out, and pay online, with separate dashboards for sellers and admins to manage products, orders, and users.

---

## Tech Stack

**Frontend:** React.js, React Router, Axios, Bootstrap 5

**Backend:** Spring Boot (Java, Spring Security, Spring Data JPA, Hibernate) and ASP.NET Core Web API (C#, Entity Framework Core)

**Database:** MySQL

**Payments:** Razorpay

---

## Features

- User registration & login
- Product & category browsing
- Cart & wishlist
- Checkout with online payment (Razorpay)
- Order placement & order history
- Seller dashboard (product & order management)
- Admin dashboard (users, sellers, products, categories, orders)
- Responsive UI

---

## Project Structure

```text
E-Mart/
│── frontend/          # React application
│── backend-spring/    # Spring Boot backend
│── backend-dotnet/    # ASP.NET Core backend
│── database/          # Database scripts
└── README.md
```

---

## Getting Started

### Clone the repo

```bash
git clone <repository-url>
cd E-Mart
```

### Frontend

```bash
cd frontend
npm install
npm run dev
```

### Spring Boot backend

```bash
cd backend-spring
mvn clean install
mvn spring-boot:run
```

### .NET backend

```bash
cd backend-dotnet
dotnet restore
dotnet run
```

---

## Database Setup

1. Install MySQL and make sure the service is running.
2. Create a database:

```sql
CREATE DATABASE emart;
```

3. Import the SQL script from the `database` folder:

```bash
mysql -u root -p emart < database/emart.sql
```

4. Update the database credentials in:
   - `backend-spring/src/main/resources/application.properties`
   - `backend-dotnet/appsettings.json`

---

## Payment Integration

Online payments are processed through **Razorpay**. The backend creates the payment order, Razorpay handles the transaction, and the result is verified server-side (via webhook) before an order is marked as paid.

Keep API keys, secrets, and DB passwords out of source control — use environment variables instead.

---

## License

This project was developed for educational purposes as part of the CDAC major project.
