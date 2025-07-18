# 🗳️ DUT Student Election System

&#x20; &#x20;

**A secure, real-time election web application designed by me and my group members exclusively for Durban University of Technology (DUT) students. I served as the Scrum Master.**

---

## 📚 Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Technology Stack](#technology-stack)
- [Project Architecture](#project-architecture)
- [Installation & Setup](#installation--setup)
- [Usage Guide](#usage-guide)
- [Live Demo](#live-demo)
- [Contributing](#contributing)
- [License](#license)
- [Author & Contact](#author--contact)
- [Acknowledgments](#acknowledgments)

---

## ✨ Overview

The DUT Student Election System is a secure online platform allowing DUT students to vote for student leaders. It ensures only verified DUT email addresses can register and vote. The system is built using Python, Flask, HTML, and CSS, with PostgreSQL as the backend.

---

## 🎯 Key Features

- ✅ Secure user authentication with email verification
- 🧑‍🎓 Student-only registration (DUT email enforcement)
- 🗳️ Real-time voting system with live results
- 📊 Vote counting and winner calculation logic
- 📓 Admin dashboard for managing elections
- 🧱 Modular architecture with Blueprints

---

## 🛠️ Technology Stack

- **Frontend**: HTML5, CSS3, JavaScript
- **Backend**: Python, Flask
- **Database**: PostgreSQL (via Render)
- **Hosting**: Render (free tier deployment)
- **Other**: Flask-Mail, Flask-WTF, Flask-Login

---

## 📂 Project Architecture

```
project/
│
├── app/
│   ├── __init__.py
│   ├── models.py
│   ├── routes/
│   ├── templates/
│   └── static/
│
├── config.py
├── requirements.txt
├── run.py
└── README.md
```

---

## 🚀 Installation & Setup

1. **Clone the repository**:

```bash
git clone https://github.com/Mbuso-ux/DUT-Election-System.git
cd DUT-Election-System
```

2. **Create a virtual environment**:

```bash
python -m venv venv
source venv/bin/activate  # on Windows: venv\Scripts\activate
```

3. **Install dependencies**:

```bash
pip install -r requirements.txt
```

4. **Configure environment variables**:

Create a `.env` file and add your:

```
SECRET_KEY=your_secret_key
MAIL_USERNAME=your_email
MAIL_PASSWORD=your_email_password
DATABASE_URL=your_postgres_url
```

5. **Run the app**:

```bash
flask run
```

---

## 📖 Usage Guide

1. Students register using their DUT email address.
2. A verification email is sent to activate the account.
3. Once verified, students can log in and vote.
4. Admins can create elections, add candidates, and view results.

---

## 🌐 Live Demo

**🟢 **[**Click here to try the live app**](https://election-gr41.onrender.com)

> Note: The free Render tier may take \~30 seconds to load.

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

- 🧾 Report bugs or issues
- ✨ Suggest new features
- 📅 Fork the repo, make changes, and submit a pull request

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 👨‍💻 Author & Contact

**Mbuso Khoza**\
📍 Durban, South Africa\
📧 [mbusokhoza575@gmail.com](mailto\:mbusokhoza575@gmail.com)\
🔗 [LinkedIn](https://www.linkedin.com/in/mbuso-khoza)\
🔗 [GitHub](https://github.com/Mbuso-ux)

---

## 🙏 Acknowledgments

- DUT IT Department and Lecturers
- Flask Documentation
- Render.com for free hosting
- Group members for collaboration and dedication

