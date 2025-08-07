Overview
This Flask-based web application provides a streamlined platform for managing GTA (Graduate Teaching Assistant) assignments. It includes features for user authentication, data import/export, course data handling, and dynamic GTA assignment generation based on predefined rules.

Features
1.	User Management:
o	User registration, login, logout, and password reset.
o	Secure password hashing with werkzeug.security.
2.	Data Import and Processing:
o	Upload course data in .xlsx or .csv formats.
o	Save, display, and edit imported course data.
o	Generate GTA assignments dynamically based on predefined rules.
3.	Dynamic GTA Assignment:
o	Automatically determine assignments based on course type, enrollment, and cross-listing.
o	Configurable rules using a JSON file (gta_rules.json).
4.	Approval Management:
o	Upload approval data files.
o	Edit approval sheet data with dynamically added columns.
o	Export data in .csv format.
5.	Cross-listing Detection:
o	Identify and handle hybrid and online course cross-listing scenarios.
6.	Interactive Features:
o	Add or remove custom columns in approval sheets.
o	Preview and modify student assignments directly from the web interface.
________________________________________
Requirements
Python Dependencies
•	Flask
•	pymongo
•	pandas
•	werkzeug
•	bson
Additional Requirements
•	MongoDB (Running on localhost:27017)
•	Excel files (.xlsx) or CSV files for data uploads.
________________________________________
Installation
1.	Clone the Repository:
    bash
    Copy code
    git clone https://github.com/Raghuram1999/GTA-APP 
    cd Milestone_3_finalcode
2.	Set Up Virtual Environment:
    
    python3 -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    pip install -r requirements.txt
3.	Database Setup:
    o	Ensure MongoDB is running locally on port 27017.
    o	The following collections will be created automatically:
	users, gta_data, gta_assignments, catalog_course, final_approval_data, columns.
4.	**Run the insertcatalogcourse.py Script: Before starting the application, you must run the insertcatalogcourse.py script to insert catalog course data into the database. This step is only required once, at the beginning of application usage:**
    bash
    python insertcatalogcourse.py
5.	Run the Application:
    python app.py
6.	Access the Application: Open http://127.0.0.1:5000 in your browser.
________________________________________
File Structure
php
Copy code
gta-management/
├── app.py                # Main application file
├── templates/            # HTML templates
├── static/               # Static files (CSS, JS)
├── uploads/              # Uploaded files directory
├── insertcatalogcourse.py # Script to populate catalog course data
├── requirements.txt      # Python dependencies
└── README.md             # Documentation
________________________________________
Configuration
1.	Secret Key: Modify the app.secret_key in app.py for better security.
2.	File Uploads: Supported file types are .xlsx and .csv. Files are saved in the uploads directory.
3.	Rules Configuration: Customize GTA assignment rules in the gta_rules.json file.
________________________________________
Usage Instructions
1.	Run Catalog Script: Ensure you run insertcatalogcourse.py before starting the application.
2.	User Management:
    o	Register an account or log in with existing credentials.
    o	Reset password if needed.
3.	Course Data Import:
    o	Navigate to "Import Course Data" and upload your file.
    o	View and verify uploaded data in the "Uploaded Data" section.
4.	Generate GTA Assignments:
    o	Generate assignments using predefined rules.
    o	Review assignments in the "View Requests" section.
5.	Approval Management:
    o	Upload approval data for review.
    o	Edit data dynamically and export as needed.
6.	Export Data:
    o	Download assignments or approval data in .csv format for external use.
________________________________________
API Endpoints
Public Endpoints
•	/ - Login page
•	/create_account - User registration
•	/forgot_password - Password recovery
Secured Endpoints
•	/import_course_data - Upload course data
•	/generate_gta_requests - Generate assignments
•	/export_requests - Export assignments as .csv
•	/upload_approval_sheet - Upload approval sheet
•	/editable_approval_sheet - Edit approval data dynamically
________________________________________
Troubleshooting
1.	MongoDB Connection:
    o	Ensure MongoDB is running on localhost:27017.
    o	Check for collection names matching the app's requirements.
2.	File Upload Errors:
    o	Ensure uploaded files are in .xlsx or .csv format.
    o	Verify the file structure matches the expected columns.
3.	Debugging: Run the app in debug mode for detailed error logs:
4.  If GTA requests are not generated, ensure the gta_rules.json file is correctly formatted and it is in correct folder.
________________________________________
Contribution
Feel free to fork the repository and create pull requests for new features or bug fixes.

