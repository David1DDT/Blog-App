Flask Blog Application

A fully functional blogging platform built with Flask, featuring user authentication, comments, and admin-only post management.

This project uses Flask, SQLAlchemy, Flask-Login, Bootstrap 5, CKEditor, and Gravatar to deliver a modern blog application.

🚀 Features

🔐 User authentication (Register, Login, Logout)

📝 Blog posts with title, subtitle, content, and images

💬 Comments system (only for logged-in users)

👑 Admin-only controls:

Create new posts

Edit existing posts

Delete posts

🎨 Rich-text editor with Flask-CKEditor

👤 User avatars with Flask-Gravatar

📱 Responsive design using Bootstrap 5

📂 Project Structure
├── app.py              # Main Flask application
├── forms.py            # Flask-WTF forms (Register, Login, CreatePost, Comment)
├── requirements.txt    # Project dependencies
├── templates/          # HTML templates (Jinja2)
│   ├── index.html
│   ├── register.html
│   ├── login.html
│   ├── post.html
│   ├── make-post.html
│   ├── about.html
│   └── contact.html
└── static/             # Static files (CSS, JS, images)

⚙️ Installation & Setup
1️⃣ Clone the repository
git clone https://github.com/your-username/flask-blog.git
cd flask-blog

2️⃣ Create and activate a virtual environment
python -m venv venv
# On Windows
venv\Scripts\activate
# On Mac/Linux
source venv/bin/activate

3️⃣ Install dependencies
pip install -r requirements.txt

4️⃣ Set environment variables

Create a .env file in the project root and add:

FLASK_KEY=your-secret-key
DB_URI=sqlite:///blog.db


Alternatively, export them in your shell:

export FLASK_KEY=your-secret-key
export DB_URI=sqlite:///blog.db

5️⃣ Run the application
flask run


The app will be available at http://127.0.0.1:5000/

👑 Admin Access

The first registered user automatically gets admin privileges (ID = 1).

Admin can:

Create new posts

Edit posts

Delete posts

📦 Dependencies

Key libraries used in this project:

Flask – Web framework

Flask-Login – User authentication

Flask-Bootstrap 5 – UI components

Flask-CKEditor – Rich-text editor

Flask-Gravatar – User avatars

Flask-SQLAlchemy – Database ORM

Werkzeug – Password hashing

All dependencies are listed in requirements.txt.

🛠️ Future Improvements

✅ Email verification for new users

✅ Password reset functionality

✅ Tagging system for posts

✅ Pagination for blog posts

📜 License

This project is licensed under the MIT License.
