# GTA Assignment Management System 
 A Flask-based web application designed to streamline the process of managing Graduate Teaching Assistant (GTA) assignments. It provides an intuitive interface for course data import/export, dynamic assignment generation, and approval workflows.  

## Overview  
This Flask-based web application streamlines the management of Graduate Teaching Assistant (GTA) assignments. It allows administrators to upload course data, apply dynamic rule-based GTA assignments, and manage approval workflows — all through a secure and interactive web interface. Designed with automation, flexibility, and usability in mind, this system reduces manual workload and increases assignment accuracy using a configurable JSON rules engine.  

## Features  
🔐 1. User Management  
👤 User registration, login, logout, and password reset  
🔒 Secure password hashing using werkzeug.security  

📁 2. Data Import and Processing  
📤 Upload .xlsx or .csv course data files  
📋 View, edit, and manage imported course data  
⚙️ Generate GTA assignments based on predefined rules  

🤖 3. Dynamic GTA Assignment  
📊 Auto-assign GTAs based on course type, enrollment size, and cross-listing  
⚙️ Rules configurable via gta_rules.json  

✅ 4. Approval Management  
📥 Upload approval data files  
🧾 Dynamically edit approval sheets with custom columns  
📤 Export final data as .csv  

🔄 5. Cross-listing Detection  
🔍 Detect hybrid and online course cross-listing scenarios  

🧩 6. Interactive Features  
➕➖ Add or remove custom columns  
👀 Preview and modify student assignments directly in the web interface  

## Requirements
**🐍 Python Dependencies**  
Flask  
pymongo  
pandas  
werkzeug  
bson  

**💾 Additional Requirements**  
🧠 MongoDB (running on localhost:27017)  
📊 Excel or CSV files for data upload    

## Key Takeaways  
✅ Automates GTA assignments based on course type, enrollment, and cross-listing.  
🔐 Includes full user management with secure authentication and password reset.  
📤 Supports .csv and .xlsx file uploads for course and approval data.  
🔄 Dynamic editing and exporting of approval sheets with custom columns.  
🧠 Uses a rules-based JSON engine (gta_rules.json) for flexible assignment logic.  
🔍 Detects cross-listed and hybrid/online courses for proper assignment handling.  
🧩 Clean interface with interactive data previews and easy navigation.  
💾 Built with Flask, MongoDB, Pandas, and Jinja2 — lightweight and extensible.  




