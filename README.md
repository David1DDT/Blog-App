<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <title>Flask Blog Application — README</title>
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <style>
    :root { --bg:#0b0c10; --card:#121318; --text:#e6e6e6; --muted:#b7b7b7; --accent:#64b5f6; }
    * { box-sizing: border-box; }
    body { margin: 0; font-family: system-ui, -apple-system, Segoe UI, Roboto, Arial, sans-serif; background: var(--bg); color: var(--text); line-height: 1.6; }
    main { max-width: 920px; margin: 0 auto; padding: 3rem 1.25rem; }
    .card { background: var(--card); border-radius: 16px; padding: 2rem; box-shadow: 0 10px 30px rgba(0,0,0,0.3); }
    h1, h2, h3 { line-height: 1.25; margin: 0 0 0.5rem; }
    h1 { font-size: 2.2rem; }
    h2 { font-size: 1.4rem; margin-top: 2rem; }
    p { color: var(--muted); margin: 0.25rem 0 1rem; }
    ul { margin: 0.25rem 0 1.25rem 1.25rem; }
    code, pre { font-family: ui-monospace, SFMono-Regular, Menlo, Consolas, "Liberation Mono", monospace; background: #0f1117; color: #eaeefb; }
    pre { padding: 1rem; border-radius: 12px; overflow: auto; border: 1px solid #1b1f2a; }
    code { padding: 0.15rem 0.35rem; border-radius: 6px; }
    .kbd { border: 1px solid #333a4a; padding: 0.12rem 0.4rem; border-radius: 6px; background: #0f1117; }
    .tag { display: inline-block; padding: 0.25rem 0.55rem; background: #0f2842; color: #cfe8ff; border: 1px solid #174a75; border-radius: 999px; font-size: 0.8rem; margin-right: .35rem; }
    .hr { height: 1px; background: #202432; border: 0; margin: 1.5rem 0; }
    a { color: var(--accent); text-decoration: none; }
  </style>
</head>
<body>
  <main>
    <article class="card">
      <header>
        <h1>Flask Blog Application</h1>
        <p>A fully functional blogging platform built with <strong>Flask</strong>, featuring user authentication, comments, and admin-only post management.</p>
        <p>This project uses <strong>Flask, SQLAlchemy, Flask-Login, Bootstrap 5, CKEditor</strong>, and <strong>Gravatar</strong> to deliver a modern blog application.</p>
        <div aria-hidden="true">
          <span class="tag">Flask</span>
          <span class="tag">SQLAlchemy</span>
          <span class="tag">Flask-Login</span>
          <span class="tag">Bootstrap 5</span>
          <span class="tag">CKEditor</span>
          <span class="tag">Gravatar</span>
        </div>
      </header>

      <div class="hr"></div>

      <section id="features">
        <h2>🚀 Features</h2>
        <ul>
          <li>🔐 User authentication (Register, Login, Logout)</li>
          <li>📝 Blog posts with title, subtitle, content, and images</li>
          <li>💬 Comments system (only for logged-in users)</li>
          <li>👑 Admin-only controls:
            <ul>
              <li>Create new posts</li>
              <li>Edit existing posts</li>
              <li>Delete posts</li>
            </ul>
          </li>
          <li>🎨 Rich-text editor with <strong>Flask-CKEditor</strong></li>
          <li>👤 User avatars with <strong>Flask-Gravatar</strong></li>
          <li>📱 Responsive design using <strong>Bootstrap 5</strong></li>
        </ul>
      </section>

      <section id="structure">
        <h2>📂 Project Structure</h2>
        <pre><code>├── app.py              # Main Flask application
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
└── static/             # Static files (CSS, JS, images)</code></pre>
      </section>

      <section id="setup">
        <h2>⚙️ Installation &amp; Setup</h2>

        <h3>1️⃣ Clone the repository</h3>
        <pre><code>git clone https://github.com/your-username/flask-blog.git
cd flask-blog</code></pre>

        <h3>2️⃣ Create and activate a virtual environment</h3>
        <pre><code>python -m venv venv
# On Windows
venv\Scripts\activate
# On Mac/Linux
source venv/bin/activate</code></pre>

        <h3>3️⃣ Install dependencies</h3>
        <pre><code>pip install -r requirements.txt</code></pre>

        <h3>4️⃣ Set environment variables</h3>
        <p>Create a <code>.env</code> file in the project root and add:</p>
        <pre><code>FLASK_KEY=your-secret-key
DB_URI=sqlite:///blog.db</code></pre>
        <p>Alternatively, export them in your shell:</p>
        <pre><code>export FLASK_KEY=your-secret-key
export DB_URI=sqlite:///blog.db</code></pre>

        <h3>5️⃣ Run the application</h3>
        <pre><code>flask run</code></pre>
        <p>The app will be available at <strong>http://127.0.0.1:5000/</strong></p>
      </section>

      <section id="admin">
        <h2>👑 Admin Access</h2>
        <ul>
          <li>The <strong>first registered user</strong> automatically gets <strong>admin privileges</strong> (ID = 1).</li>
          <li>Admin can create, edit, and delete posts.</li>
        </ul>
      </section>

      <section id="dependencies">
        <h2>📦 Dependencies</h2>
        <p>Key libraries used in this project:</p>
        <ul>
          <li><strong>Flask</strong> – Web framework</li>
          <li><strong>Flask-Login</strong> – User authentication</li>
          <li><strong>Flask-Bootstrap 5</strong> – UI components</li>
          <li><strong>Flask-CKEditor</strong> – Rich-text editor</li>
          <li><strong>Flask-Gravatar</strong> – User avatars</li>
          <li><strong>Flask-SQLAlchemy</strong> – Database ORM</li>
          <li><strong>Werkzeug</strong> – Password hashing</li>
        </ul>
        <p>All dependencies are listed in <code>requirements.txt</code>.</p>
      </section>

      <section id="roadmap">
        <h2>🛠️ Future Improvements</h2>
        <ul>
          <li>✅ Email verification for new users</li>
          <li>✅ Password reset functionality</li>
          <li>✅ Tagging system for posts</li>
          <li>✅ Pagination for blog posts</li>
        </ul>
      </section>

      <section id="license">
        <h2>📜 License</h2>
        <p>This project is licensed under the <strong>MIT License</strong>.</p>
      </section>
    </article>
  </main>
</body>
</html>
