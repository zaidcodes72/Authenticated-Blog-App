# 📝 Django Blog App  

Welcome to **MyBlog**, a fully functional and modern blog platform built with **Django**. This app allows users to register, log in, log out, create blog posts, update their profile, and reset their password — all in a responsive Bootstrap-styled UI.  

---

## ✨ Features  

### 🔐 **User Authentication**  
✅ Register, Login, Logout  
✅ Unique email validation during signup  
✅ Password reset via email (SMTP)  

### 👤 **Profile Management**  
✏️ Users can update their username, email, and profile image
👀 Profile images are displayed next to blog posts 

### ✍️ **Blog Functionality**  
📝 **CRUD** (Create, Read, Update, Delete) blog posts  
🔗 Posts linked to authors  
📄 Detail pages for individual posts   
📄 Pagination for both all posts and posts by specific users 

### ⚙️ **Admin Panel**  
🛠️ Manage users and blog posts from the Django admin interface 

### 🎨 **UI/UX**  
📱 Responsive design (Bootstrap)  
🎨 Crispy Forms for better form styling  

### 📧 **Email Integration**  
✉️ Gmail SMTP for password resets  
🛡️ `.env` secure configuration  

---

## 🛠️ Tech Stack  

| Category       | Technology       |
|---------------|-----------------|
| **Backend**   | Django v5.x       |
| **Frontend**  | Bootstrap v5.x     |
| **Database**  | SQLite (current) / PostgreSQL (In Future) |
| **Deployment**| Heroku-ready    |
| **Email**     | Gmail SMTP      |

---


## 📁 Project Structure

```
├── blog/                      # Blog app: handles posts
│   ├── migrations/
│   ├── static/
│   │   └── blog/
│   │       ├── main.css
│   ├── templates/
│   │   └── blog/
│   │       ├── base.html
│   │       ├── home.html
│   │       ├── about.html
│   │       ├── post_detail.html
│   │       ├── post_form.html
│   │       ├── post_confirm_delete.html
│   │       ├── user_posts.html
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── models.py
│   ├── tests.py
│   ├── urls.py
│   └── views.py

├── users/                     # Users app: handles auth & profiles
│   ├── migrations/
│   ├── templates/
│   │   └── users/
│   │       ├── register.html
│   │       ├── login.html
│   │       ├── logout.html
│   │       ├── profile.html
│   │       ├── password_reset.html
│   │       ├── password_reset_done.html
│   │       ├── password_reset_confirm.html
│   │       └── password_reset_complete.html
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── signals.py
│   ├── models.py
│   ├── tests.py
│   ├── urls.py
│   └── views.py

├── myblog/                    # Main project settings folder
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py

├── media/                     # Uploaded profile images (via MEDIA_ROOT)
│   └── profile_pics/

├── templates/                 # Global template dir (optional)
│   └── 404.html, 500.html, etc.

├── .myvenv                    # Hidden file for environment variables (not pushed to GitHub)
├── .env                   
├── .gitignore
├── db.sqlite3
├── manage.py
├── posts.json
├── README.md
└── requirements.txt

```


## 🚀 Installation & Setup  

1. **Clone the repository**
   ```bash
   git clone https://github.com/zaidcodes72/Authenticated-Blog-App.git
   cd Authenticated-Blog-App
   ```

2. **Create virtual environment**
   ```bash
    python -m venv venv
    source venv/bin/activate  # Linux/Mac
    venv\Scripts\activate     # Windows
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Apply migrations**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Create superuser (optional)**
   ```bash
   python manage.py createsuperuser
   ```
   

6. **Run development server**
   ```bash
   python manage.py runserver
   ```
   Access the application at `http://localhost:8000`