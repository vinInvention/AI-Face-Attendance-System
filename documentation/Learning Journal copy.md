# Lesson 1

✔ Application versions

There are three versions to this AIFAS system
VERSION 1:
Platform: Laptop/Desktop
Laptop Webcam
│
▼
OpenCV
│
▼
Face Recognition
│
▼
SQLite Database
│
├── Excel Report
└── Gmail Notification

Learning objective:

Python
OpenCV
Face recognition
SQLite
Tkinter
Excel automation
Email automation

without introducing networking, embedded systems, or distributed computing.

This version is about mastering the fundamentals.

VERSION 2:
Version 2 (Networked AI Attendance System)

Introduce networking.

IP Camera
│
▼
Network
│
▼
Laptop Server
│
▼
AI Recognition
│
▼
Database

Learning objective:

IP cameras
RTSP video streams
Multiple cameras
Network programming
Centralized processing

This is much closer to what many organizations use.

VERSION 3:

Camera
│
ESP32 / Raspberry Pi
│
Runs AI locally
│
Recognizes face
│
Sends attendance event
│
Wi-Fi
│
Cloud Server
│
Online Database
│
Google Sheets
│
Admin Dashboard

This is a true Edge AI + IoT system.

# Lesson 2

✔ GitHub Repository

What I learned

• Why GitHub is important
• Repository structure
• README
• Project planning

Challenges

# Lesson 2

✔ Compiling the modules of the project
Modules are the different units of the project that handle specific tasks. In the case of the AIFAS software, the modules are the different files that have the extension .py, and which will do a specific task. The modules in this project are:

1. User Interface (Tkinter)

Responsible for:

Buttons
Menus
Windows
Messages

It does not recognize faces.

2. Camera Module

Responsible for:

Opening webcam
Capturing frames

Nothing else.

3. Vision Module

Responsible for:

Detecting faces
Recognizing faces

It does not save attendance.

4. Attendance Module

Responsible for:

Recording attendance
Preventing duplicates
Determining late status

It does not send emails.

5. Database Module

Responsible for:

Saving staff
Reading attendance
Searching records

Nothing else.

6. Report Module

Responsible for:

Excel reports
Monthly reports 7. Email Module

Responsible for:

Sending Gmail notifications
Sending monthly summaries

# Links to Ai helper

1. https://chatgpt.com/c/6a3cf65a-c6e0-83ea-a399-8ab9adc6a194
2. https://ln.run/NzRcd
