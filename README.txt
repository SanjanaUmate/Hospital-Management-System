Hospital Management System - Java + MySQL

Files included:
- HospitalManagementSystem.java (main class)
- Doctor.java
- Patient.java

Instructions:
1. Setup MySQL database named 'hospital'
2. Create tables: doctors, patients, appointments (see below)
3. Modify DB credentials in HospitalManagementSystem.java if needed
4. Compile all Java files and run HospitalManagementSystem

Sample SQL to create tables:

CREATE DATABASE hospital;
USE hospital;

CREATE TABLE doctors (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    specialization VARCHAR(100)
);

CREATE TABLE patients (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    age INT,
    gender VARCHAR(10)
);

CREATE TABLE appointments (
    id INT PRIMARY KEY AUTO_INCREMENT,
    patient_id INT,
    doctor_id INT,
    appointment_date DATE,
    FOREIGN KEY (patient_id) REFERENCES patients(id),
    FOREIGN KEY (doctor_id) REFERENCES doctors(id)
);

Add some sample data to doctors table for testing:

INSERT INTO doctors (name, specialization) VALUES ('Dr. Smith', 'Cardiology'), ('Dr. Jane', 'Neurology');

Run the program and test the options.