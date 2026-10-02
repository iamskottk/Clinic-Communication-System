# 🏥 ClinicCallSystem

### Clinic Call Communication System

**A local network communication solution for healthcare environments.**

A Python-based clinic communication system that allows a doctor to send prescription, patient file, laboratory result and assistance requests from an iPhone to a receptionist's computer. Requests are displayed on a central dashboard, where they can be acknowledged, processed and completed.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square\&logo=python\&logoColor=white) ![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square\&logo=flask\&logoColor=white) ![SQLite](https://img.shields.io/badge/Database-SQLite-003B57?style=flat-square\&logo=sqlite\&logoColor=white) ![PWA](https://img.shields.io/badge/Mobile-PWA-5A0FC8?style=flat-square) ![Status](https://img.shields.io/badge/Status-In_Development-orange?style=flat-square)

---

## 🚀 Features

| Feature                    | Description                                    |
| -------------------------- | ---------------------------------------------- |
| 📱 Doctor Mobile Interface | Submit requests from an iPhone                 |
| 💊 Prescription Requests   | Notify reception when a prescription is needed |
| 📁 Patient File Requests   | Request patient files                          |
| 🧪 Laboratory Requests     | Request laboratory results                     |
| 🆘 Assistance Requests     | Request general assistance                     |
| 🚨 Urgent Assistance       | Flag urgent requests for attention             |
| 🔔 Notifications & Sound   | Alert reception to incoming requests           |
| 📳 Vibration Feedback      | Provide mobile feedback where supported        |
| ✅ Request Acknowledgement  | Confirm that a request has been received       |
| ✔️ Request Completion      | Track completed requests                       |
| ❌ Cancellation             | Cancel requests when necessary                 |
| 📊 Statistics & History    | Review request activity and status             |
| 🟢 Doctor Online Status    | Display doctor availability                    |
| 💾 SQLite Database         | Store requests and history locally             |

## ⚙️ Technologies

`Python` · `Flask` · `HTML5` · `CSS3` · `JavaScript` · `SQLite` · `PWA` · `TCP/IP Networking`

## 🔄 How It Works

```text
┌─────────────────────────┐
│   DOCTOR'S IPHONE       │
│   Select Request        │
└────────────┬────────────┘
             │
             ▼
┌─────────────────────────┐
│   FLASK WEB SERVER      │
│   Local Clinic Network  │
└────────────┬────────────┘
             │
             ▼
┌─────────────────────────┐
│   RECEPTION DASHBOARD   │
│   Notification Received │
└────────────┬────────────┘
             │
             ▼
┌─────────────────────────┐
│ ACKNOWLEDGE & PROCESS   │
│   Complete or Cancel    │
└─────────────────────────┘
```

**Request lifecycle:** `PENDING` → `ACKNOWLEDGED` → `COMPLETED`

Requests may also be cancelled when necessary.

## 📂 Project Structure

```text
ClinicCallSystem/
├── app.py
├── templates/
│   ├── index.html
│   ├── doctor.html
│   └── reception.html
├── static/
│   ├── style.css
│   ├── doctor.js
│   └── reception.js
├── clinic_calls.db
└── README.md
```

## 🛠️ Installation & Setup

**Requirements:** Python installed on the reception computer and both devices connected to the same clinic network.

**1. Install Flask**

```bash
py -m pip install flask
```

**2. Start the application**

```bash
py app.py
```

Configure Flask to listen on `0.0.0.0:5000` for local network access.

**3. Open the receptionist dashboard**

```text
http://127.0.0.1:5000/reception
```

**4. Find the reception computer's IP address**

```bash
ipconfig
```

**5. Open the doctor interface on the iPhone**

```text
http://YOUR-PC-IP:5000/doctor
```

Replace `YOUR-PC-IP` with the reception computer's actual local IPv4 address.

> **Important:** Allow access through the computer's firewall only on the trusted clinic network. The server must be configured to expose the required routes before the application can be used.

## 📲 Mobile App Experience

The doctor interface is designed for mobile use and can be installed on the iPhone Home Screen through Safari.

1. Open the doctor interface in Safari.
2. Tap **Share**.
3. Select **Add to Home Screen**.
4. Launch the application from the Home Screen.

A complete Progressive Web App experience requires the appropriate web app manifest and other PWA assets. Vibration and notification behavior may vary depending on the browser and iOS version.

## 🧪 Testing

| Component                    | Status   |
| ---------------------------- | -------- |
| Doctor Mobile Interface      | ✅ Tested |
| Reception Dashboard          | ✅ Tested |
| Request Delivery             | ✅ Tested |
| Urgent Requests              | ✅ Tested |
| Notifications and Sound        | ✅ Tested |
| Acknowledge / Complete       | ✅ Tested |
| Request Cancellation         | ✅ Tested |
| Request History              | ✅ Tested |
| Statistics                   | ✅ Tested |
| Clinic Network Communication | ✅ Tested |

## 🔐 Security Considerations

This project is intended for controlled local-network use. Before deployment in a live healthcare environment, implement and verify:

* User authentication and role-based access control.
* HTTPS and secure session management.
* Audit logging and access restrictions.
* Database protection and encrypted backups.
* Firewall rules and authorised-device controls.
* Data minimisation and appropriate retention policies.

**Privacy note:** Avoid including patient names, medical record numbers, diagnoses or other identifying clinical information in general request messages.

## 🔮 Future Development

`Multi-Doctor Support` · `Multiple Clinic Rooms` · `Authentication` · `WebSocket Notifications` · `Audit Logs` · `Advanced Reporting` · `Automated Backups` · `Centralised Administration` · `Enhanced Security`

## 🎯 Project Objective

To develop a practical communication tool that reduces repeated calls and interruptions, improves request visibility and helps clinic staff coordinate routine and urgent tasks using existing computer and mobile infrastructure.

**Skills demonstrated:** Software Development · Web Technologies · Networking · Database Management · System Administration · Mobile Technology · Cybersecurity Awareness

## 👨‍💻 Author

**Kabo Sekoto**
BSc (Hons) Information Technology
Master's in Cybersecurity — In Progress

---

*ClinicCallSystem — Improving communication, supporting coordination and streamlining clinic workflows.*
