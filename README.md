# Flask Blog Application

A fully functional **Flask-based blog application** with user authentication, rich-text editing, comments, and admin-only post management.  
Built with **Flask, SQLAlchemy, Flask-Login, Flask-Bootstrap, and CKEditor**.

---

## 📂 Project Structure

```plaintext
flask-blog/
│
├── venv/                   # Virtual environment (not pushed to GitHub)
│
├── app.py                  # Main Flask application
├── forms.py                # WTForms definitions
├── requirements.txt        # Python dependencies
├── README.md               # Project documentation
│
├── templates/              # HTML templates (Jinja2)
│   ├── base.html
│   ├── index.html
│   ├── post.html
│   ├── register.html
│   ├── login.html
│   ├── make-post.html
│   ├── about.html
│   └── contact.html
│
└── static/                 # Static files (CSS, JS, Images)
    ├── styles.css
    └── ...
🚀 Features
📝 Blog Posts
Create, edit, and delete posts (admin only)

Rich-text editor with Flask-CKEditor

👤 User Authentication
Register and login securely with hashed passwords

Flask-Login session management

💬 Comments
Logged-in users can comment on posts

Comments linked to posts and users

🔑 Admin-only Routes
Only the admin (user ID = 1) can manage posts

🎨 UI Enhancements
Bootstrap 5 integration

Gravatar for user avatars

⚙️ Installation
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/flask-blog.git
cd flask-blog
2. Set Up Virtual Environment
bash
Copy
Edit
python -m venv venv
Activate it:

Windows (PowerShell):

bash
Copy
Edit
venv\Scripts\activate
Mac/Linux:

bash
Copy
Edit
source venv/bin/activate
3. Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
4. Configure Environment Variables
Create a .env file in the project root with:

ini
Copy
Edit
FLASK_KEY=your_secret_key
DB_URI=sqlite:///blog.db
▶️ Usage
Run the app:

bash
Copy
Edit
python app.py
Visit in your browser:

cpp
Copy
Edit
http://127.0.0.1:5000/
Default routes:

/ → Homepage with all posts

/register → Register new users

/login → Login page

/new-post → Create new post (admin only)

/about → About page

/contact → Contact page

📦 Requirements
Here’s the content of requirements.txt:

txt
Copy
Edit
Flask
Flask-Bootstrap
Flask-Login
Flask-WTF
Flask-CKEditor
Flask-Gravatar
Flask-SQLAlchemy
Werkzeug
python-dotenv
Install them with:

bash
Copy
Edit
pip install -r requirements.txt
🤝 Contribution
Contributions are welcome!

Fork the repo

Create a new branch (feature/awesome-feature)

Commit changes (git commit -m "Add awesome feature")

Push to branch (git push origin feature/awesome-feature)

Open a Pull Request

📜 License
This project is licensed under the MIT License.
Feel free to use and modify it for your own projects.
