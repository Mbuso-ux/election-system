
# 🗳️ Election System for DUT Students

[![Python](https://img.shields.io/badge/python-3.12-blue)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/flask-3.1.0-lightgrey)](https://flask.palletsprojects.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

A secure, real-time election web application **designed exclusively for Durban University of Technology (DUT) students**. This system enables verified DUT students to register, authenticate via their university emails, and vote for their student leaders representing various parties.

---

## 🚀 Features

- 🔐 **Email verification restricts signup to DUT students only**  
- 🏛️ Admin dashboard for managing elections, parties, candidates, and positions  
- 🗳️ Voter dashboard with profile, voting, and history  
- ⚡ Real-time vote tallying and election results with SocketIO  
- 📧 Email notifications for registration, verification, and voting events  
- 🔄 Database migrations with Alembic & SQLAlchemy ORM  
- 🧩 Modular Flask Blueprints architecture  

---

## 🛠️ Tech Stack

| Layer          | Technology                        |
|----------------|---------------------------------|
| Backend        | Python, Flask                   |
| Authentication | Flask-Login, Flask-Bcrypt       |
| Real-time      | Flask-SocketIO                  |
| Database       | SQLAlchemy ORM, Alembic Migrations |
| Email          | Flask-Mail                     |
| Frontend       | Jinja2 templates, Bootstrap CSS |
| Deployment     | `runserver.py` (SocketIO server) |

---

## 📂 Project Structure

```
flaskappenv/
├── app/
│   ├── __init__.py               # Application factory
│   ├── runserver.py             # Entry point
│   ├── models/                  # SQLAlchemy models
│   │   ├── user.py
│   │   ├── vote.py
│   │   └── ...
│   ├── routes/                  # Flask Blueprints
│   │   ├── admin_routes.py
│   │   ├── auth_routes.py
│   │   └── ...
│   ├── services/                # Email and other services
│   │   └── email_service.py
│   ├── static/images/           # Images and assets
│   ├── templates/               # Jinja2 templates
│   │   ├── admin/
│   │   ├── candidate/
│   │   └── voter/
│   ├── app.db                  # SQLite database file
│   ├── cli.py                  # CLI commands
│   ├── config.py               # App config
│   └── extensions.py           # Flask extensions
├── migrations/                 # Alembic migrations
├── requirements.txt            # Dependencies
├── runserver.py                # Main runner
├── Procfile                    # For deployment
├── README.md                   # This file
└── .gitignore                  # Git ignore
```

---

## 🧪 Installation & Setup

```bash
git clone https://github.com/Mbuso-ux/election-system.git
cd election-system/flaskappenv

python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

pip install -r requirements.txt

# Set environment variables in a .env file or your OS
# SECRET_KEY, MAIL_SERVER, MAIL_PORT, MAIL_USERNAME, MAIL_PASSWORD, etc.

flask db upgrade

python runserver.py
```

---

## 📖 Usage

- Register using your **DUT student email** (verification required)  
- Login to vote for your preferred leaders from different parties  
- View live election results as voting progresses  
- Admins oversee elections and candidate management  

---

## 🌐 Live Demo

The application is deployed and available at:  
[election-gr41.onrender.com](https://election-gr41.onrender.com)

---

## 📸 Screenshots

*Add screenshots here to showcase your app’s UI.*

---

## 🤝 Contributing

Feel free to submit issues or pull requests. Please fork the repo and open a PR for review.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Mbuso Khoza**  
📧 mbusokhoza575@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/mbuso-khoza) | [GitHub](https://github.com/Mbuso-ux)

---
