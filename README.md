# 🚗 Car Rental Management System (Database Architecture & Design)

[![Database](https://img.shields.io/badge/Database-SQL_Server-blue.svg)](https://www.microsoft.com/en-us/sql-server/)
[![Diagram Tools](https://img.shields.io/badge/Design_Tool-Draw.io-orange.svg)](https://app.diagrams.net/)
[![Architecture](https://img.shields.io/badge/Architecture-ERD_%26_Relational-green.svg)](#-architecture--design)

Welcome to the **Car Rental Management System** database design project! This repository contains a comprehensive Relational Database Schema and Entity-Relationship Diagram (ERD) designed to streamline and automate the operations of a modern car rental agency. 

Included in this repository is the complete **SQL Server Backup / Database File** allowing you to restore, test, and query the system directly in your environment!

---

## 📖 Table of Contents
- [📌 Overview](#-overview)
- [⚙️ Core Operations](#️-core-operations)
- [💡 Key Concepts Demonstrated](#-key-concepts-demonstrated)
- [🏗️ Architecture & Design](#️-architecture--design)
- [🛠️ Technologies Used](#️-technologies-used)
- [🚀 How to Use / Restore Data](#-how-to-use--restore-data)

---

## 📌 Overview

Managing a car rental fleet requires robust data integrity, seamless tracking of vehicle availability, customer histories, rental bookings, and financial transactions. 

This project provides a fully normalized, scalable, and well-structured database schema. It models the complete lifecycle of a rental process—from customer registration and vehicle management to booking, returns, additional charges, and payment tracking.

---

## ⚙️ Core Operations

The database design handles the following core business workflows in detail:

### 1. 🚘 Vehicle & Fleet Management
* **Vehicle Categorization:** Tracks vehicle specs (Make, Model, Year, Fuel Type, Transmission, Mileage).
* **Availability Tracking:** Real-time status monitoring (Available, Rented, Under Maintenance).
* **Pricing Models:** Daily rate management per vehicle category/type.

### 2. 👤 Customer Management
* **Profile Records:** Stores essential customer details (Full Name, Contact Info, Driver's License Details).
* **Rental History:** Tracks previous bookings, returns, and payment reliability.

### 3. 📅 Booking & Rental Lifecycle
* **Reservation System:** Records pick-up/drop-off dates, locations, and initial rental calculations.
* **Active Rentals:** Manages active rental agreements, initial deposits, and expected return schedules.

### 4. 🔄 Returns & Financial Settlement
* **Check-In Inspection:** Records return condition, actual drop-off time, and mileage.
* **Additional Charges:** Automatically factors in late fees, damage assessments, fuel surcharges, or extra mileage.
* **Payments & Refunds:** Calculates final balances, total paid amount, and refunds/remaining dues.

---

## 💡 Key Concepts Demonstrated

This project showcases fundamental and advanced database engineering concepts:

* **Entity-Relationship Modeling (ERD):** Conceptual and logical data modeling crafted using **Draw.io**.
* **Database Normalization (3NF):** Elimination of data redundancy and update anomalies to ensure structural efficiency.
* **Referential Integrity & Constraints:** Strict Foreign Key constraints, Primary Keys, Unique Keys, and Check Constraints.
* **Transactional Integrity:** Designed to support atomic operations for booking, check-outs, and return payments.
* **Scalable Schema Design:** Modular table relationships allowing easy extension for future features (e.g., Insurance, Maintenance Logs).

---

## 🏗️ Architecture & Design

The system is designed with a clear separation of entities:
    
    [ Customer ] ─── (1:N) ───< [ Booking / Rental ] >─── (N:1) ─── [ Vehicle ]
          │
        (1:1)
          │
    [ Return & Payment ]


* **Primary Entities:** `Customers`, `Vehicles`, `Bookings` (or `Rentals`), `Returns`, `Payments`.
* **Diagram:** Designed precisely using **Draw.io** to map out cardinalities, attributes, and key relationships.

---

## 🛠️ Technologies & Tools Used

* **Design & Modeling:** [Draw.io](https://app.diagrams.net/)
* **Database Management System (DBMS):** Microsoft SQL Server (MSSQL)
* **Language:** T-SQL (Transact-SQL)
* **Version Control:** Git & GitHub

---

## 🚀 How to Use / Restore Data

To test the database with pre-populated data:

1. Open SQL Server Management Studio (SSMS).

2. Restore the .bak file or attach the .mdf file included in the repository:

    * Right-click Databases > Restore Database... (or Attach...).

    * Select the file provided in this project.

3. Execute queries, test constraints, and explore the schema!

---

## 🙏 Acknowledgments

This project is part of the Programming Advices Training Track led by:

    👨‍🏫 Dr. Mohamed Abouhadhood
    💻 Platform: Programming Advices

