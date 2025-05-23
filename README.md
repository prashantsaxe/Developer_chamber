# Developer Chamber

Developer Chamber is a full-stack social networking platform designed for developers to connect, share posts, and showcase their professional profiles. It includes user authentication, profile management, posts, and a real-time interactive user experience. The backend is built using Django REST Framework, and the frontend leverages React with Redux for state management.

## Table of Contents

- [Features](#features)
- [Technologies](#technologies)
- [Project Structure](#project-structure)
- [Setup Instructions](#setup-instructions)
- [Running the Application](#running-the-application)
- [Testing](#testing)
- [Environment Variables](#environment-variables)
- [Contributing](#contributing)
- [License](#license)

## Features

- User registration and login with JWT authentication
- Create and manage developer profiles
- Add experience and education details
- Create, like, comment on posts
- View other developer profiles and posts
- Responsive UI using React
- State management with Redux

## Technologies

**Backend:** Python, Django, Django REST Framework  
**Frontend:** React, Redux, JavaScript, CSS  
**Authentication:** JWT  
**Dev Tools:** VSCode, Git, GitHub  
**Testing:** Django test framework

## Project Structure

```
prashantsaxe-developer_chamber/
├── LICENSE
├── README.md               # Project documentation
├── backend/                # Django backend
│   ├── manage.py
│   ├── requirements.txt
│   ├── devconnector/       # Core app logic
│   │   ├── models.py       # Data models
│   │   ├── serializers.py  # DRF serializers
│   │   ├── views.py        # API views
│   │   ├── urls.py         # API routes
│   │   └── utils.py        # Utility functions
│   └── mysite/             # Django settings and configuration
├── frontend/               # React frontend
│   ├── public/             # Static assets
│   ├── src/
│   │   ├── components/     # Reusable components
│   │   ├── actions/        # Redux actions
│   │   ├── reducers/       # Redux reducers
│   │   ├── store.js        # Redux store
│   │   └── utils/          # Utility scripts
│   └── package.json        # Frontend dependencies
└── .vscode/                # Editor configuration
```

## Setup Instructions

### Prerequisites

- Python 3.8+
- Node.js & npm
- Virtualenv (recommended)
- Git

### Backend Setup

```bash
cd backend
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

### Frontend Setup

```bash
cd frontend
npm install
npm start
```

## Running the Application

- Backend: [http://localhost:8000](http://localhost:8000)
- Frontend: [http://localhost:3000](http://localhost:3000)

## Testing

Run backend tests using Django:

```bash
cd backend
python manage.py test
```

## Environment Variables

Update the Django `settings.py` file with:

- `SECRET_KEY`
- `DEBUG`
- `ALLOWED_HOSTS`
- Database configuration if not using default SQLite

Frontend uses a proxy setup in `package.json` to forward API calls to the backend.

## Contributing

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/YourFeature`
3. Commit your changes: `git commit -m 'Add YourFeature'`
4. Push to the branch: `git push origin feature/YourFeature`
5. Open a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
