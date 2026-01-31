# SerenitySpace 🧘‍♀️

A peaceful mental wellness web application built with Django, designed to help users cultivate mindfulness, gratitude, and inner calm through journaling and reflection.

## 🌟 Features

### Current Capabilities

-   **Journaling System**: Write and store personal journal entries with timestamps
-   **Calm Prompts**: Access guided prompts for meditation and reflection
-   **Gratitude Practice**: Record daily gratitude notes to foster positivity
-   **Audio Integration**: Built-in calming audio player with meditation sounds
-   **Breathing Exercises**: Interactive breathing guidance tools
-   **Clean, Minimal Interface**: Serene design focused on user tranquility

## 🚀 Getting Started

### Prerequisites

-   Python 3.8 or higher
-   pip (Python package manager)

### Installation

1.  **Clone or extract the repository**
    
    ```bash
    unzip SerenitySpace.zip
    cd SerenitySpace
    ```
    
2.  **Create a virtual environment** (recommended)
    
    ```bash
    python -m venv venv
    
    # On Windows:
    venv\Scripts\activate
    
    # On macOS/Linux:
    source venv/bin/activate
    ```
    
3.  **Install dependencies**
    
    ```bash
    pip install -r requirements.txt
    ```
    
4.  **Run database migrations**
    
    ```bash
    python manage.py migrate
    ```
    
5.  **Collect static files** (for production)
    
    ```bash
    python manage.py collectstatic
    ```
    
6.  **Start the development server**
    
    ```bash
    python manage.py runserver
    ```
    
7.  **Access the application** Open your browser and navigate to: `http://127.0.0.1:8000`

## 📁 Project Structure

```
SerenitySpace/
├── SerenitySpace/          # Main project directory
│   ├── settings.py        # Django settings and configuration
│   ├── urls.py            # Main URL routing
│   └── wsgi.py            # WSGI configuration
├── calmcore/              # Core application module
│   ├── models.py          # Database models (JournalEntry, CalmPrompt, Gratitude)
│   ├── views.py           # View functions and logic
│   ├── urls.py            # App-specific URL routing
│   ├── admin.py           # Django admin configuration
│   ├── templates/         # HTML templates
│   │   └── calmcore/
│   │       ├── home.html  # Landing page
│   │       └── journal.html # Journal interface
│   └── static/            # Static assets
│       └── calmcore/
│           ├── style.css  # Custom styles
│           ├── audio.js   # Audio player functionality
│           └── audio/     # Audio files
│               └── calm.mp3
├── staticfiles/           # Collected static files
├── db.sqlite3             # SQLite database (default)
└── manage.py              # Django management script
```

## 🗄️ Database Models

### JournalEntry

-   `text`: TextField - The journal entry content
-   `created_at`: DateTimeField - Automatic timestamp

### CalmPrompt

-   `prompt`: TextField - Guided meditation or reflection prompt
-   `created_at`: DateTimeField - Automatic timestamp

### Gratitude

-   `note`: TextField - Gratitude entry content
-   `created_at`: DateTimeField - Automatic timestamp

## 🎨 Customization

### Styling

-   Edit `calmcore/static/calmcore/style.css` to customize the visual design
-   The app uses a calming color palette with blues and greens

### Audio

-   Replace or add audio files in `calmcore/static/calmcore/audio/`
-   Update `audio.js` to reference new audio files

### Content

-   Modify templates in `calmcore/templates/calmcore/` to change page layouts
-   Add new models in `calmcore/models.py` for additional features

## 🔧 Configuration

### Settings (`SerenitySpace/settings.py`)

-   Database configuration (default: SQLite)
-   Static files settings
-   Installed applications
-   Middleware configuration

### Database

By default, SerenitySpace uses SQLite for simplicity. To switch to PostgreSQL, MySQL, or other databases:

1.  Install the appropriate database adapter
2.  Update `DATABASES` in `settings.py`
3.  Run migrations again

## 🌐 Deployment

### For Production Deployment

1.  **Set environment variables**
    
    ```bash
    export DEBUG=False
    export SECRET_KEY='your-secret-key'
    export ALLOWED_HOSTS='yourdomain.com'
    ```
    
2.  **Use a production database** (PostgreSQL recommended)
3.  **Serve static files** with a web server (Nginx, Apache)
4.  **Use a WSGI server** (Gunicorn, uWSGI)
    
    ```bash
    pip install gunicorn
    gunicorn SerenitySpace.wsgi:application
    ```
    
5.  **Configure security settings**
    -   Set `DEBUG = False`
    -   Configure `ALLOWED_HOSTS`
    -   Use HTTPS
    -   Set up proper CSRF and security settings

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## 📝 License

This project is open source and available under the MIT License.

## 🙏 Acknowledgments

-   Built with Django - The web framework for perfectionists with deadlines
-   Inspired by the growing need for accessible mental wellness tools
-   Designed to promote mindfulness and emotional well-being

##