# 🎬 Movie-Log

A full stack movie tracking web app that lets you discover, search, and save your favourite films.

---

## 📸 Screenshots

### Login Page
![Login Page](screenshots/login.png)

### Home Page
![Home Page](screenshots/home.png)

### Favourites Page
![Favourites Page](screenshots/favourites.png)

---

## ✨ Features

- 🔐 User Authentication (Signup & Login with JWT)
- 🎬 Browse popular and trending movies
- 🔍 Search movies by title
- ❤️ Add and remove movies from favourites
- 💾 Favourites saved to database — persist after refresh
- 📱 Responsive UI with dark theme

---

## 🛠️ Tech Stack

### Frontend
| Technology | Purpose |
|---|---|
| React | UI Framework |
| React Router | Page Navigation |
| Context API | Global State Management |
| Bootstrap | Styling & Responsive Layout |
| TMDB API | Movie Data |

### Backend
| Technology | Purpose |
|---|---|
| Django | Backend Framework |
| Django REST Framework | REST API |
| Simple JWT | Authentication |
| SQLite | Database |

---

## 🚀 Getting Started

### Prerequisites
- Node.js
- Python 3.x
- TMDB API Key (free at [themoviedb.org](https://www.themoviedb.org/))

---

### Frontend Setup

```bash
# Clone the repo
git clone https://github.com/hasnainazam/movie-log.git

# Go to frontend folder
cd movie-log/frontend

# Install dependencies
npm install

# Create .env file
VITE_API_KEY=your_tmdb_api_key_here

# Run the app
npm run dev
```

---

### Backend Setup

```bash
# Go to backend folder
cd movie-log/backend

# Create virtual environment
python -m venv .venv
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Run migrations
python manage.py migrate

# Create superuser
python manage.py createsuperuser

# Run the server
python manage.py runserver
```

---

## 📁 Project Structure

```
movie-log/
├── frontend/
│   ├── src/
│   │   ├── Components/
│   │   │   ├── Card.jsx
│   │   │   └── Navbar.jsx
│   │   ├── Pages/
│   │   │   ├── Home.jsx
│   │   │   ├── Favourites.jsx
│   │   │   └── Login.jsx
│   │   ├── contexts/
│   │   │   └── MovieContext.jsx
│   │   └── App.jsx
│   └── package.json
│
└── backend/
    ├── movies/
    │   ├── models.py
    │   ├── views.py
    │   ├── serializers.py
    │   └── urls.py
    ├── movielog/
    │   ├── settings.py
    │   └── urls.py
    └── manage.py
```

---

## 🔌 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/signup/` | Register new user |
| POST | `/api/token/` | Login and get JWT token |
| POST | `/api/token/refresh/` | Refresh JWT token |
| GET | `/api/favorites/` | Get user's favourites |
| POST | `/api/favorites/add/` | Add a favourite |
| DELETE | `/api/favorites/remove/<id>/` | Remove a favourite |

---

## 👤 Author

**Hasnain Azam**
- GitHub: [@hasnainazam](https://github.com/hasnainazam)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
