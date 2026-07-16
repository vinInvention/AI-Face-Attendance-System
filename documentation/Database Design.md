# Tables

Here is the solution to my assignment:
To make your system future-proof, I have designed these tables so they work perfectly right now, but can scale up to my Networked (V2) and Edge AI (V3) versions without needing a complete redesign later.

1. users Table (Administrator Accounts)This table stores the credentials for the admins who can log into the Tkinter Dashboard.
   id (INTEGER, PK, Autoincrement): Unique database row ID.
   username (TEXT, Unique, Not Null): Login username.
   password_hash (TEXT, Not Null): Encrypted password string.
   email (TEXT, Unique): For recovery alerts.
   created_at (DATETIME, Default Current Timestamp).

2. staff Table (The People Being Tracked)This table holds the profiles of employees or students. It links their personal info to their AI face profile.
   id (INTEGER, PK, Autoincrement): Internal tracking key.
   staff_num (TEXT, Unique, Not Null): Your official company ID format (e.g., EMP001).
   first_name (TEXT, Not Null).
   last_name (TEXT, Not Null).
   department (TEXT): For department filters (e.g., "HR").
   status (TEXT, Default 'Active'): Sets profile to 'Active' or 'Inactive'.
   created_at (DATETIME, Default Current Timestamp).

3. face_profiles Table The file path to where their image is stored. Because one person doesn't have one face image.
   id (INTEGER, PK, Autoincrement): Unique photo entry ID.
   staff_id (INTEGER, FK referencing staff(id)): Connects photo to the employee.
   image_path (TEXT, Not Null): Path to raw reference file.
   encoding_path (TEXT, Not Null): Path to the saved 128-d face embedding array file.
   created_at (DATETIME, Default Current Timestamp).

4. attendance Table (The Logs)This table records every single time the camera successfully recognizes a face.
   id (INTEGER, Primary Key, Autoincrement): Unique log ID.
   staff_id (INTEGER, Foreign Key referencing staff(id)): Links the clock-in to a specific staff member.
   date (TEXT, Not Null): The exact day (YYYY-MM-DD). Separating date makes daily Excel reports much faster to generate.
   time (TEXT, Not Null): The exact clock-in time (HH:MM:SS).
   status (TEXT): Can mark them as 'Present', 'Late', or 'On Time' based on company rules.
   device_id (TEXT, Default 'Local_Webcam'): Crucial for V2 and V3. This tracks which camera or edge node logged the attendance.

5. settings Table (System Configurations)Instead of hardcoding rules into the Python files, save them here so the admin can change them via the Tkinter UI.
   key (TEXT, Primary Key): The name of the setting (e.g., 'work_start_time', 'admin_gmail', 'recognition_threshold').
   value (TEXT): The actual setting rule (e.g., '09:00:00', 'admin@gmail.com', '0.6').

Your suggestion that we work in 2 weeks sprint is a welcomed suggestion.
