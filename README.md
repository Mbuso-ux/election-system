# 🗳️ DUT Student Election System

<div align="center">

[![Python](https://img.shields.io/badge/python-3.12-blue?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/flask-3.1.0-000000?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](LICENSE)
[![Live Demo](https://img.shields.io/badge/Live%20Demo-Available-brightgreen?style=for-the-badge&logo=render)](https://election-gr41.onrender.com)

**A secure, real-time election web application designed by me and my group members exclusively for Durban University of Technology (DUT) students in which I was a scrum master**

</div>

---

## 📚 Table of Contents

- [✨ Overview](#️-overview)
- [🎯 Key Features](#️-key-features)
- [🛠️ Technology Stack](#️-technology-stack)
- [📂 Project Architecture](#-project-architecture)
- [🚀 Installation & Setup](#installation--setup)
- [📖 Usage Guide](#️-usage-guide)
- [🌐 Live Demo](#️-live-demo)
- [🤝 Contributing](#contributing)
- [📄 License](#license)
- [👨‍💻 Author & Contact](#️-author--contact)
- [🙏 Acknowledgments](#️-acknowledgments)

---


## ✨ Overview

The DUT Student Election System is a comprehensive web application that enables verified DUT students to participate in democratic student leadership elections. With robust authentication, real-time voting, and administrative oversight, this platform ensures fair and transparent elections for the university community.

## 🎯 Key Features

### 🔐 **Authentication & Security**
- **DUT-exclusive registration** with university email verification
- Secure password hashing with Flask-Bcrypt
- Session management with Flask-Login
- Email verification workflow for account activation

### 🏛️ **Administrative Control**
- Complete election management dashboard
- Party and candidate registration system
- Position management and configuration
- Real-time monitoring and oversight tools

### 🗳️ **Voting Experience**
- Intuitive voter dashboard with profile management
- Secure ballot casting with verification
- Comprehensive voting history tracking
- Live election results and analytics

### ⚡ **Real-time Features**
- Live vote tallying with Flask-SocketIO
- Instant result updates during elections
- Real-time participant notifications
- Dynamic dashboard updates

### 📧 **Communication System**
- Automated email notifications for registration
- Vote confirmation and receipt emails
- Election announcements and updates
- System status notifications

---

## 🛠️ Technology Stack

<div align="center">

| **Layer** | **Technology** | **Purpose** |
|-----------|----------------|-------------|
| **Backend** | Python 3.12, Flask 3.1.0 | Core application framework |
| **Authentication** | Flask-Login, Flask-Bcrypt | User management & security |
| **Real-time** | Flask-SocketIO | Live updates & notifications |
| **Database** | SQLAlchemy ORM, Alembic | Data persistence & migrations |
| **Email** | Flask-Mail | Communication system |
| **Frontend** | Jinja2, Bootstrap 5 | Template rendering & styling |
| **Deployment** | Render.com | Production hosting |

</div>

---

## 📂 Project Architecture

```
flaskappenv/
├── 🚀 app/
│   ├── __init__.py              # Application factory & configuration
│   ├── runserver.py            # Main application entry point
│   │
│   ├── 📊 models/              # Data models & database schema
│   │   ├── user.py            # User authentication model
│   │   ├── vote.py            # Voting records model
│   │   ├── candidate.py       # Candidate information model
│   │   └── election.py        # Election management model
│   │
│   ├── 🛣️ routes/              # Flask blueprints & API endpoints
│   │   ├── admin_routes.py    # Administrative dashboard
│   │   ├── auth_routes.py     # Authentication workflows
│   │   ├── voter_routes.py    # Voter dashboard & voting
│   │   └── api_routes.py      # RESTful API endpoints
│   │
│   ├── 📧 services/            # Business logic & external services
│   │   ├── email_service.py   # Email notification system
│   │   ├── auth_service.py    # Authentication utilities
│   │   └── vote_service.py    # Vote processing logic
│   │
│   ├── 🎨 static/              # Frontend assets
│   │   ├── css/               # Custom stylesheets
│   │   ├── js/                # JavaScript & SocketIO client
│   │   └── images/            # Application assets
│   │
│   ├── 📄 templates/           # Jinja2 template hierarchy
│   │   ├── base.html          # Base template layout
│   │   ├── admin/             # Administrative interface
│   │   ├── voter/             # Voter dashboard & voting
│   │   └── auth/              # Authentication pages
│   │
│   ├── 🗄️ app.db               # SQLite database file
│   ├── ⚙️ config.py            # Application configuration
│   ├── 🔧 extensions.py        # Flask extension initialization
│   └── 💻 cli.py               # Custom CLI commands
│
├── 🔄 migrations/              # Alembic database migrations
├── 📋 requirements.txt         # Python dependencies
├── 🚀 runserver.py            # Production server runner
├── 📦 Procfile               # Deployment configuration
└── 📖 README.md              # Project documentation
```

---

## 🚀 Installation & Setup

### Prerequisites
- Python 3.12 or higher
- Git
- Virtual environment tool

### Quick Start

```bash
# 1️⃣ Clone the repository
git clone https://github.com/Mbuso-ux/election-system.git
cd election-system/flaskappenv

# 2️⃣ Create and activate virtual environment
python -m venv venv

# On Windows
venv\Scripts\activate

# On macOS/Linux
source venv/bin/activate

# 3️⃣ Install dependencies
pip install -r requirements.txt

# 4️⃣ Set up environment variables
# Create a .env file with the following:
```

### Environment Configuration

Create a `.env` file in the project root:

```bash
# Application Settings
SECRET_KEY=your-secret-key-here
FLASK_ENV=development
FLASK_APP=app

# Database Configuration
DATABASE_URL=sqlite:///app.db

# Email Configuration (for notifications)
MAIL_SERVER=smtp.gmail.com
MAIL_PORT=587
MAIL_USE_TLS=True
MAIL_USERNAME=your-email@gmail.com
MAIL_PASSWORD=your-app-password

# DUT Domain Restriction
ALLOWED_DOMAIN=dut4life.ac.za
```

### Database Setup

```bash
# Initialize database and run migrations
flask db upgrade

# (Optional) Create sample data
python -c "from app.cli import create_sample_data; create_sample_data()"
```

### Launch Application

```bash
# Development server
python runserver.py

# The application will be available at http://localhost:5000
```

---

## 📖 Usage Guide

### 👨‍🎓 For Students

1. **Registration**
   - Visit the registration page
   - Use your **DUT student email** (@dut4life.ac.za)
   - Complete email verification process
   - Set up your secure password

2. **Voting Process**
   - Log in to your voter dashboard
   - Browse available elections and positions
   - Review candidate profiles and manifestos
   - Cast your vote securely
   - Receive confirmation via email

3. **Track Results**
   - View real-time election results
   - Access your voting history
   - Monitor election progress and updates

### 👨‍💼 For Administrators

1. **Election Management**
   - Create and configure elections
   - Set voting periods and eligibility criteria
   - Monitor participation and system health

2. **Candidate Management**
   - Register parties and candidates
   - Manage position assignments
   - Review and approve candidate profiles

3. **System Oversight**
   - Monitor voting activity in real-time
   - Generate reports and analytics
   - Manage user accounts and permissions

---

## 🌐 Live Demo

The application is deployed and fully operational at:

**🔗 [election-gr41.onrender.com](https://election-gr41.onrender.com)**

*Test the system using the demo credentials provided on the login page*

---

## 🤝 Contributing

We welcome contributions from the DUT community! Here's how you can help:

### Development Setup
1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Make your changes and commit: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

### Contribution Guidelines
- Follow PEP 8 style guidelines for Python code
- Write comprehensive tests for new features
- Update documentation for any API changes
- Ensure all tests pass before submitting PR

### Issues & Bug Reports
- Use the GitHub issue tracker
- Provide detailed reproduction steps
- Include system information and error logs
- Tag issues appropriately (bug, feature, enhancement)

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for complete details.

```
MIT License - Copyright (c) 2024 Mbuso Khoza
Permission is hereby granted, free of charge, to any person obtaining a copy...
```

---

## 👨‍💻 Author & Contact

<div align="center">

**Mbuso Khoza**  
*Full-Stack Developer & DUT Student*

[![Email](https://img.shields.io/badge/Email-mbusokhoza575@gmail.com-red?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mbusokhoza575@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mbuso%20Khoza-blue?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mbuso-khoza)
[![GitHub](https://img.shields.io/badge/GitHub-Mbuso--ux-black?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Mbuso-ux)

</div>

---

## 🙏 Acknowledgments

- **Durban University of Technology** for inspiring this project
- **Flask Community** for excellent documentation and support
- **Open Source Contributors** who make projects like this possible
- **Group Members** who made this project a success
  

---

<div align="center">

*Empowering student democracy through technology*

</div>
