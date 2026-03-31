# 📏 Quantity Measurement App
**A Full-Stack Spring Boot & React Application for Unit Normalization**

---

## 📖 Project Overview
The **Quantity Measurement App** is a specialized engineering tool designed to solve the problem of **Unit Normalization**. In complex systems, data often arrives in inconsistent formats (e.g., mixing Inches and Feet). This application provides a unified logic layer to standardize, compare, and perform mathematical operations on these quantities with scientific precision.

---

## 🌟 Core Features

### ⚖️ Precision Measurement Logic 
* **Dimensional Analysis:** Supports multiple measurement categories including **Length, Weight, Volume, and Temperature**.
* **Base Unit Normalization:** Implements a backend strategy that scales all inputs to a common "Base Unit" before processing, ensuring accurate comparisons (e.g., verifying that `12 Inches` equals `1 Foot`).
* **Arithmetic Engine:** A robust calculation layer capable of adding, subtracting, multiplying, or dividing quantities with automatic unit handling.

### 🔐 Security & User Management
* **JWT Authentication:** Uses **JSON Web Tokens** to maintain secure, stateless communication between the React frontend and Spring Boot backend.
* **Google OAuth2 Integration:** Provides a modern "Login with Google" feature, allowing for seamless user onboarding and identity verification.
* **Access Control:** Protects sensitive data, ensuring that only logged-in users can view or manage their calculation history.

### 📊 Smart Data Persistence
* **Database Tracking:** Every calculation and comparison is automatically logged into a **MySQL database** for future reference.
* **Contextual Navigation:** The interface intelligently hides or shows the "History" link based on the user's current task (e.g., visible only during Comparison mode).
* **History Management:** A dedicated, full-screen history view allows users to review past results in a structured table or perform a full database wipe.

---

## 🛠️ Architectural Components

### **Backend (Spring Boot 3)**
* **RESTful Controller:** Handles API requests and returns structured JSON responses.
* **Spring Security:** Manages the application firewall, JWT validation, and Google OAuth2 filters.
* **Spring Data JPA:** Simplifies data persistence by mapping Java objects directly to MySQL tables.
* **Validation Layer:** Ensures all incoming measurement data follows strict formatting rules before reaching the database.

### **Frontend (React.js)**
* **Component-Based UI:** Built with reusable React components for a modular and maintainable codebase.
* **State Management:** Uses React Hooks (`useState`, `useEffect`) to provide real-time updates without page refreshes.
* **Responsive Styling:** Combines **Bootstrap 5** with custom CSS to ensure a professional look across mobile and desktop screens.
* **Axios Integration:** Facilitates secure, asynchronous communication with the backend API.

