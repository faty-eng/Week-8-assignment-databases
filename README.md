
---

# 📋 Clinic Booking System – Relational Database

## 📌 Project Overview

This project is a **relational database management system (RDBMS)** built using **MySQL** for a **Clinic Booking System**. It is designed to manage and store information related to doctors, patients, appointments, treatments, and doctor specializations. The database is structured to support real-world use cases such as booking appointments, tracking treatments, and managing doctor specialties.

---

## 🎯 Objective

* Design and implement a **full-featured relational database**.
* Use **SQL** to define tables, constraints, and relationships.
* Apply proper **normalization** principles and **data integrity constraints**.

---

## 🧱 Database Schema Overview

### ✔️ Entity Tables:

| Table Name               | Description                                      |
| ------------------------ | ------------------------------------------------ |
| `Doctors`                | Stores doctor information                        |
| `Patients`               | Stores patient information                       |
| `Appointments`           | Links doctors and patients with scheduled visits |
| `Treatments`             | Records treatments given during appointments     |
| `Specializations`        | List of medical specializations                  |
| `Doctor_Specialization`  | Links doctors to their specialties (M\:M)        |
| `Medications` (Optional) | Tracks medicines used in treatments              |

---

## 🔗 Entity Relationships

* **Doctors ↔ Appointments**: One-to-Many (a doctor can have many appointments)
* **Patients ↔ Appointments**: One-to-Many (a patient can have many appointments)
* **Appointments ↔ Treatments**: One-to-Many (an appointment can have many treatments)
* **Doctors ↔ Specializations**: Many-to-Many (a doctor can have multiple specialties)
* **Treatments ↔ Medications** *(Optional)*: One-to-Many

---

## ⚙️ SQL Features Used

* `CREATE DATABASE`
* `CREATE TABLE`
* **Constraints**:

  * `PRIMARY KEY`
  * `FOREIGN KEY`
  * `NOT NULL`
  * `UNIQUE`
* **Many-to-Many Relationship** via junction table (`Doctor_Specialization`)
* **Auto-incrementing IDs** for unique identifiers

---

## 📁 File Structure

```
project-folder/
│
├── clinic_booking_system.sql   -- SQL script to create the database
└── README.md                   -- Project description and documentation
```

---

## ✅ How to Run

1. Open your MySQL client (MySQL Workbench, phpMyAdmin, CLI, etc.)
2. Run the script file:

   ```sql
   SOURCE path_to/clinic_booking_system.sql;
   ```
3. The database `clinic_booking` will be created with all tables and relationships set up.

---

## 🔒 Data Integrity & Validation

* All fields such as `email`, `phone` have `UNIQUE` constraints where applicable.
* Foreign key constraints ensure referential integrity between related tables.
* Junction tables ensure normalized many-to-many relationships.

---

## 🧪 Testing Tips (Optional)

You can test the database with simple `INSERT` statements like:

```sql
INSERT INTO Doctors (name, phone, email) VALUES ('Dr. Sarah Lee', '1234567890', 'slee@clinic.com');
INSERT INTO Patients (name, date_of_birth, phone, email) VALUES ('John Doe', '1990-01-01', '9876543210', 'johndoe@email.com');
```

And then create an appointment:

```sql
INSERT INTO Appointments (doctor_id, patient_id, appointment_date, reason)
VALUES (1, 1, '2025-10-01 10:00:00', 'General Checkup');
```

---

## 📚 Future Enhancements

* Add authentication layer for doctors/patients (e.g., login credentials)
* Include billing & invoice tracking
* Track room/slot availability for scheduling
* Front-end interface for patient booking

---

## 👨‍💻 Author

**\[FATIMA-ZAHRA]**
Relational Database Systems – Assignment 8
Course: \[Build a Complete Database Management System]
Date: September 2025

---

## 📄 License

This project is for academic and educational use only.

