# HospitalManagementSystem
HospitalManagementSystem
HospitalManagementSystem is a Java-based console application that helps manage hospital operations efficiently. It supports adding and viewing patient details, viewing available doctors, and booking appointments between patients and doctors. The system uses MySQL as the backend database and interacts with it using JDBC.

Project Requirements & Functionalities:-
Requirements:
       Java JDK 8 or higher
       MySQL Database
       JDBC Driver (MySQL Connector/J)
       IDE (Eclipse, IntelliJ, VS Code, etc.)

Functionalities:
1.Add Patient-
      Input and store patient name, age, and gender.

2.View Patients-
      Display all registered patients from the database in tabular format.

3.View Doctors-
      Show all doctors with their specializations.

4.Book Appointment-
      Book an appointment between a patient and doctor on a specific date.
      Ensures doctor availability and existence of patient/doctor.

5.Exit-
     Close the application.

Technologies & Concepts Used:-
Java: Core application logic.
JDBC (Java Database Connectivity): Connecting Java with MySQL.
MySQL: Backend relational database.
Object-Oriented Programming: Classes, objects, methods, encapsulation.
Exception Handling: Try-catch blocks for safe execution.
Command Line Interface: For user interaction using Scanner.



Project Structure & Explanation
1. HospitalManagementSystem.java
   Main class that:
   Connects to the MySQL database.
   Presents menu options.
   Handles user interaction and routing.

2. Patient.java
   Handles:
   Adding new patient data.
   Viewing all patients.
   Checking if a patient exists by ID.

3. Doctor.java
   Handles:
   Viewing doctor details.
   Checking if a doctor exists by ID.

4. MySQL Database Tables
   CREATE TABLE patients (
   id INT PRIMARY KEY AUTO_INCREMENT,
   name VARCHAR(100),
   age INT,
   gender VARCHAR(10)
   );

CREATE TABLE doctors (
id INT PRIMARY KEY AUTO_INCREMENT,
name VARCHAR(100),
specialization VARCHAR(100)
);

CREATE TABLE appointments (
id INT PRIMARY KEY AUTO_INCREMENT,
patient_id INT,
doctor_id INT,
appointment_date DATE,
FOREIGN KEY (patient_id) REFERENCES patients(id),
FOREIGN KEY (doctor_id) REFERENCES doctors(id)
);


Application Flow
START
↓
Display Main Menu
↓
User selects option:
→ Add Patient
→ View Patients
→ View Doctors
→ Book Appointment
→ Exit
↓
Perform respective function
↓
Return to Menu or Exit

Summary-
The Hospital Management System project is a beginner-friendly, database-integrated Java console application. It simplifies hospital tasks such as storing and retrieving patient/doctor data and managing appointments. With real-time database operations and clear validation, it ensures proper scheduling and recordkeeping in a hospital setting. This project is ideal for learning database connectivity (JDBC), object-oriented design, and real-world application development in Java.
