🏥 Clinic Call Communication System
A local-network clinic communication system that allows doctors to send service requests from an iPhone directly to a receptionist dashboard.
The system was developed to solve a simple but common problem in clinic operations: doctors having to verbally call reception whenever they need a prescription, patient file, laboratory results or assistance.

📌 Overview
The Clinic Call Communication System connects a doctor's mobile device to a receptionist computer through the clinic's local Wi-Fi network.
The doctor uses an iPhone as a controller, while reception staff use a computer-based dashboard to receive, acknowledge and complete requests.

┌──────────────────┐
│   Doctor iPhone  │
│                  │
│ Send Request     │
└────────┬─────────┘
         │
         │ Clinic Wi-Fi
         ▼
┌──────────────────┐
│  Flask Server    │
│    Python        │
└────────┬─────────┘
         │
         ▼
┌──────────────────┐
│ Reception PC     │
│                  │
│ Manage Requests  │
└──────────────────┘

✨ Features
📱 Doctor mobile interface
🖥️ Receptionist dashboard
💊 Prescription requests
📁 Patient file requests
🧪 Laboratory result requests
🆘 Assistance requests
🚨 Urgent assistance requests
🔔 New request notifications
🔊 Notification sounds
✅ Request acknowledgement
✔️ Request completion
❌ Request cancellation
📊 Request statistics
🕒 Request history
🟢 Doctor online status
📲 App-style mobile interface
📳 Vibration feedback
💾 SQLite database
🛠️ Technologies
Python
Flask
HTML5
CSS3
JavaScript
SQLite
Progressive Web App (PWA)
Local TCP/IP Networking
📂 Project Structure
ClinicCallSystem/
│
├── app.py
│
├── templates/
│   ├── index.html
│   ├── doctor.html
│   └── reception.html
│
├── static/
│   ├── style.css
│   ├── doctor.js
│   └── reception.js
│
├── clinic_calls.db
│
└── README.md

⚙️ How It Works
Doctor
The doctor opens the application on an iPhone and selects the required service.
For example:

Prescription
Patient File
Laboratory Results
Assistance
Urgent Assistance

After submitting the request, it is sent to the Flask server running on the reception computer.
Reception
The receptionist dashboard receives the request and displays:
Doctor
Room
Request type
Priority
Time
Current status
The receptionist can then acknowledge and process the request.
Request Lifecycle
PENDING
   ↓
ACKNOWLEDGED
   ↓
COMPLETED

Requests can also be cancelled when necessary.
🚀 Installation
Make sure Python is installed on the reception computer.
Install Flask:

py -m pip install flask

Start the application:
py app.py

The server listens on:
0.0.0.0:5000

Open the receptionist dashboard:
http://127.0.0.1:5000/reception

Find the computer's IP address:
ipconfig

Then open the doctor interface on the iPhone:
http://YOUR-PC-IP:5000/doctor

Both devices must be connected to the same clinic network.
📱 Mobile App
The doctor interface supports an app-style experience using a Progressive Web App.
On iPhone:

Open the doctor interface in Safari.
Tap Share.
Select Add to Home Screen.
Launch the system from the Home Screen.
This allows the doctor to use the system similarly to a normal mobile application without requiring an App Store installation.
🔐 Security Considerations
The current system is designed for a controlled local-network environment.
Recommended security improvements for future versions include:

User authentication
Role-based access control
HTTPS
Session management
Audit logging
Database encryption
Automated backups
Improved network security
Access restrictions for authorised devices
Patient-identifying or unnecessary medical information should not be entered into general request messages.
🧪 Testing
The system was tested across the main communication workflow:
Doctor → Send Request
          ↓
Reception → Receive Request
          ↓
Reception → Acknowledge
          ↓
Reception → Complete

Tested functionality includes:
Doctor interface
Reception dashboard
Request submission
Request notifications
Urgent requests
Acknowledgement
Completion
Cancellation
Request history
Statistics
Mobile access
Local-network communication
📸 Screenshots
Doctor Interface
Add screenshot here
Reception Dashboard
Add screenshot here
Mobile Home Screen
Add screenshot here
Request Notification
Add screenshot here
🔮 Future Development
Planned improvements include:
Multi-doctor support
Multiple clinic rooms
User login and authentication
Real-time WebSocket communication
Advanced reporting
Audit logs
Automated backups
Centralised administration
Dedicated Android/iOS application
Enhanced cybersecurity controls
🎯 Project Objective
The objective of this project is to demonstrate how a practical software solution can be developed to improve communication and workflow within a healthcare environment using existing clinic infrastructure.
The project combines:

Web Development • Python • Networking • Database Management • System Administration • Mobile Technology • Cybersecurity

👨‍💻 Author
Kabo Sekoto
BSc (Hons) Information Technology
Master's in Cybersecurity

Clinic Call Communication System
A practical IT solution designed to improve communication and workflow within a clinic.
