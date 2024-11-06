Student Management System in C++

This README file provides an overview and setup instructions for the Student Management System project using C++ and MySQL. This project is a simple console-based application that can manage student records efficiently, featuring functionalities for adding, updating, viewing, searching, and deleting student information.
Project Overview

    Project Name: Student Management System in C++
    Abstract: A console-based project to help colleges or universities manage student details.
    Language Used: C++
    IDE: Code::Blocks (Version 16.01)
    Database: MySQL (managed via XAMPP)
    Type: Console Application
    Level: Recommended for beginners and intermediate learners of C++

Features

    Admin Login:
        Admin can log in using the credentials:
            Username: admin
            Password: admin
    CRUD Operations:
        Add: Admin can add new student records.
        View: View all existing student records.
        Update: Admin can update existing student details.
        Delete: Admin can delete student records.
    Search: Search for specific student details using roll numbers.
    Admin Protection: Only authorized admin users can add or update records.

Setup Instructions
Prerequisites

Ensure you have the following software installed:

    Dev C++ (Optional, based on your preference)
    Code::Blocks IDE (Version 16.01)
    XAMPP (For managing MySQL database)

Development Environment Setup

    Install Code::Blocks:
        Download and install Code::Blocks (version 16.01).
    Install XAMPP:
        Download and install XAMPP from the official site.
        Open XAMPP and start Apache and MySQL services.
    Setup MySQL Database:
        Open a browser and go to localhost/phpmyadmin/.
        Execute the following SQL commands to set up the database:

CREATE DATABASE studentmanagement;
USE studentmanagement;

CREATE TABLE userdetail (
    username VARCHAR(20),
    password VARCHAR(20)
);
INSERT INTO userdetail (username, password) VALUES ('admin', 'admin');

CREATE TABLE studentdetails (
    studentno INT PRIMARY KEY,
    firstname VARCHAR(20),
    lastname VARCHAR(20),
    mobileno VARCHAR(20),
    course VARCHAR(20),
    stream VARCHAR(20)
);

INSERT INTO studentdetails (studentno, firstname, lastname, mobileno, course, stream)
VALUES
    (1, 'Rees', 'Thomas', '8230954239', 'BTech', 'CSE'),
    (2, 'Geogre', 'Okal', '0987654321', 'BTech', 'IT'),
    (3, 'Eli', 'Ochieng', '1234567890', 'BTech', 'ECE'),
    (4, 'Raphael', 'Sagwe', '0987654321', 'BTech', 'EEE'),
    (5, 'Rono', 'Boan', '0987654321`', 'BTech', 'IT');

Code Implementation

    Open Code::Blocks:
        Create a new project named StudentManagement.
        Copy and paste the provided C++ code into the main.cpp file.
    Compile and Run:
        Build and run the project in Code::Blocks.
        Use the menu to navigate through the options for managing student records.

Using the Application

    Start the Application:
        Run the application and select options from the menu.
    Administrator Login:
        Log in with the username admin and password admin.
    Manage Student Records:
        Use options to add, view, update, search, or delete student records.
    Logout and Exit:
        Logout to secure the system or exit the application when done.

Notes

    Ensure the MySQL server is running in XAMPP before launching the application.
    This project uses simple console-based input/output, making it easy to understand for beginners.

Troubleshooting

    Database Connection Issues:
        Make sure XAMPP's MySQL service is active.
        Double-check the database name and table structures in phpMyAdmin.
    Login Issues:
        Verify that the admin credentials are correctly inserted into the database.
    Code Compilation Errors:
        Ensure you have included all necessary header files and linked the MySQL library correctly in Code::Blocks.

Enjoy coding and managing student records with this simple and effective project
