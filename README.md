# ☕ Café Management System – Java (JFrame + MySQL)

A fully functional **Café Management System** built using **Java Swing (JFrame)** and **MySQL**.  
This desktop application helps manage café operations such as user authentication, menu items, categories, billing, and order management.

This project was developed as part of learning Java GUI development and MySQL database connectivity.

---

## 🚀 Features

### 🔐 User Authentication
- Signup (create new account)  
- Login (with database validation)  
- Forgot Password  
- Password reset using security question  

### 🍽 Product & Category Management
- Add new category  
- Add new products  
- Update product details  
- Delete items  
- Auto-refreshing product list  

### 🧾 Order & Billing System
- Select products and create an order  
- Auto-calculate total amount  
- Apply tax / GST (if configured)  
- Generate printable bill  
- Save bill details into database  
- Unique bill IDs  

### 📊 Dashboard / Home Screen
- Modern UI with navigation  
- Access to product management, order page, billing page  
- Menu-driven interface  

### 🎨 User Interface (Swing)
- JFrame-based forms  
- Icons and images for improved UI  
- Loading animations (popupicon)  
- Clean and easy-to-use layout  

---

## 🛠️ Tech Stack

| Component | Technology |
|----------|------------|
| Programming Language | Java |
| GUI Framework | Java Swing / JFrame |
| Database | MySQL |
| ORM | JDBC |
| IDE Used | NetBeans |
| Build System | Ant (build.xml) |

---

## 📁 Project Folder Structure

```
CafeManagementSystem/
│
├── src/
│   ├── cafe/ms/               # All UI screens (JFrames)
│   ├── common/                # Utility classes
│   ├── dao/                   # Database operations (DAO classes)
│   ├── image/                 # Icons and application images
│   ├── model/                 # Java model classes (POJOs)
│   └── popupicon/             # Loading screen graphics
│
├── build/                     # Auto-generated (NetBeans)
├── lib/                       # Required jar files (optional)
├── nbproject/                 # NetBeans project config
├── manifest.mf
├── build.xml                  # Ant build script
└── LICENSE
```

---

## 🗄 Database Structure (MySQL)

Your project expects a database named **cafe**.

### Tables  

#### 1. `user`
| Field | Type |
|-------|------|
| id | int (PK) |
| name | varchar |
| email | varchar |
| mobileNumber | varchar |
| password | varchar |
| securityQuestion | varchar |
| answer | varchar |
| status | varchar |

#### 2. `category`
| Field | Type |
|-------|------|
| id | int (PK) |
| name | varchar |

#### 3. `product`
| Field | Type |
|-------|------|
| id | int (PK) |
| name | varchar |
| category | varchar |
| price | int |

#### 4. `bill`
| Field | Type |
|-------|------|
| id | int (PK) |
| name | varchar |
| mobileNumber | varchar |
| email | varchar |
| date | varchar |
| total | varchar |
| createdBy | varchar |

---

## ⚙️ Installation & Setup

### 1️⃣ Install Dependencies
- Java JDK 8 or above  
- MySQL Server + Workbench  
- NetBeans IDE (recommended)

### 2️⃣ Create Database

```sql
CREATE DATABASE cafe;
```

### 3️⃣ Configure JDBC Connection

```java
String url = "jdbc:mysql://localhost:3306/cafe";
String username = "root";
String password = "YOUR_PASSWORD";
```

Add **MySQL Connector JAR** to project libraries.

### 4️⃣ Run the Application
- Open the project in NetBeans  
- Clean and Build  
- Run `Signup.java` to create first user  
- Then run `Login.java`  

---

## 🔮 Future Enhancements
- Admin role & permissions  
- Export bill as PDF  
- Inventory management  
- Employee management  
- More modern UI using JavaFX  
- Sales analytics & charts  

---

## 🤝 Contributing
Pull requests are welcome.  
Feel free to improve features or UI.

---

## 📝 License
This project is licensed under the **MIT License**.

