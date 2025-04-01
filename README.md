# Online-Voting System

An online voting system built with Django that allows users to participate in elections electronically.

## Features

- User authentication and registration
- Admin dashboard for election management
- Secure voting process
- Real-time results and analytics
- Mobile-responsive design

## Requirements

- Python 3.8+
- Django 4.0+
- Other dependencies (listed in requirements.txt)

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/online-voting-system.git
   cd online-voting-system
   ```

2. Create and activate a virtual environment (optional but recommended):
   ```
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Configure the database:
   ```
   python manage.py makemigrations
   python manage.py migrate
   ```

5. Create a superuser (admin account):
   ```
   python manage.py createsuperuser
   ```

6. Start the development server:
   ```
   python manage.py runserver
   ```

7. Access the application:
   - Main site: http://127.0.0.1:8000/
   - Admin dashboard: http://127.0.0.1:8000/admin/

## Usage

### Admin Functions
- Create and manage elections
- Add candidates
- Set voting timeframes
- View and analyze results

### Voter Functions
- Register and login
- View active elections
- Cast votes securely
- View election results (if enabled by admin)

## Project Structure

```
online-voting-system/
├── manage.py
├── requirements.txt
├── voting_system/           # Main project folder
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── elections/               # Elections app
│   ├── migrations/
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   └── templates/
├── users/                   # Users app
│   ├── migrations/
│   ├── models.py
│   ├── views.py
│   └── templates/
└── static/                  # Static files
    ├── css/
    ├── js/
    └── images/
```

## Customization

You can customize various aspects of the system:

- Modify templates in the `templates` directory
- Update CSS in the `static/css` directory
- Add or modify models in `models.py` files

## Security Features

- CSRF protection
- Password hashing
- Session management
- Form validation

## Troubleshooting

### Common Issues:

1. **Database migration errors**:
   - Delete the migration files (except `__init__.py`) and try again
   - Ensure your database configuration is correct

2. **Static files not loading**:
   - Check `STATIC_URL` and `STATICFILES_DIRS` in settings.py
   - Run `python manage.py collectstatic`

3. **Port already in use**:
   - Change the port: `python manage.py runserver 8080`

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request


## Acknowledgements

- Django framework
- Bootstrap for frontend
- FontAwesome icons
- Contributors and supporters
