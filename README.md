

# Flask Blog Application

A fully functional Python/Flask web application to create, manage, and comment on blog posts.  
Includes user authentication and admin-only post management with rich-text editing.

## Features
- User registration and login with password hashing
- Create, edit, and delete blog posts (admin only)
- Comment on posts (for logged-in users)
- Rich-text editor with Flask-CKEditor
- Bootstrap 5 for responsive UI
- Gravatar integration for user avatars

## Requirements
- Python 3.x
- Flask
- Flask-Bootstrap
- Flask-Login
- Flask-WTF
- Flask-CKEditor
- Flask-Gravatar
- Flask-SQLAlchemy
- Werkzeug
- python-dotenv

## Setup

1. Clone the repository:
```bash
git clone https://github.com/your-username/flask-blog.git
cd flask-blog
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
# Windows
venv\Scripts\activate
# Mac/Linux
source venv/bin/activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Create a .env file in the project root with the following:
```bash
FLASK_KEY=your_secret_key
DB_URI=sqlite:///blog.db
```
## Usage

- Run the app:

```bash
python app.py
```

- Open your browser and go to:

```bash
http://127.0.0.1:5000/
```

- Default routes:
  - `/` → Homepage with all posts
  - `/register` → Register a new user
  - `/login` → Login page
  - `/new-post` → Create a new post (admin only)
  - `/edit-post/<post_id>` → Edit post (admin only)
  - `/delete/<post_id>` → Delete post (admin only)
  - `/about` → About page
  - `/contact` → Contact page

## Project Structure
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
```
## Notes

- The first registered user is the admin by default.
- Only logged-in users can comment on posts.
- Database URI can be updated in the `.env` file to use other databases (PostgreSQL, MySQL, etc.).
- For production deployment, disable debug mode and configure a proper secret key.

## License

This project is licensed under the MIT License.


