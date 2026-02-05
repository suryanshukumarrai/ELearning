E-Learning Platform
A comprehensive Django-based E-Learning platform designed for remedial teaching and capacity building programs. This system provides course management, online testing, instructor profiles, and student progress tracking.

Features
📚 Course Management
Create and manage educational courses/programs
Associate courses with instructors
Enroll participants in courses
Track course start dates and duration
Course descriptions and detailed information
👨‍🏫 Instructor Management
Instructor profiles with bio and credentials
Video introduction support (YouTube/Vimeo links)
Featured instructor showcase on homepage
Instructor listing and search functionality
📝 Testing & Assessment
Create tests/quizzes for courses
Multiple choice questions with correct answer marking
Timed tests with duration settings
Student test submissions and automatic grading
Test result viewing with score calculation
Track attempted tests history
👥 User Management
User registration and authentication
Student profiles with unique registration numbers
User dashboard with personalized information
Profile editing capabilities
Secure login/logout system
🔧 Additional Features
Problem reporting system for students
Participant management and enrollment
Responsive design with Bootstrap styling
Search functionality for courses and instructors
Admin panel for content management
Tech Stack
Backend: Django 5.2.4
Database: SQLite3
Frontend: HTML5, CSS3, JavaScript
Styling: Bootstrap 5, Custom CSS
Authentication: Django Auth System
Project Structure
E-Learning/
├── manage.py                 # Django management script
├── db.sqlite3               # SQLite database
├── Project/                 # Main project configuration
│   ├── settings.py         # Django settings
│   ├── urls.py             # Root URL configuration
│   └── wsgi.py             # WSGI configuration
├── programs/                # Main application
│   ├── models.py           # Database models
│   ├── views.py            # View functions and classes
│   ├── urls.py             # App URL patterns
│   ├── forms.py            # Django forms
│   ├── admin.py            # Admin configuration
│   ├── templates/          # HTML templates
│   │   ├── programs/       # App-specific templates
│   │   └── registration/   # Auth templates
│   ├── fixtures/           # Sample data files
│   └── migrations/         # Database migrations
└── static/                  # Static files
    ├── css/                # Stylesheets
    ├── js/                 # JavaScript files
    └── images/             # Image assets
Installation & Setup
Prerequisites
Python 3.8 or higher
pip (Python package manager)
Installation Steps
Clone the repository

git clone https://github.com/suryanshukumarrai/ELearning.git
cd e-learnig/E-Learning
Create a virtual environment (recommended)

python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Install Django

pip install django
Run database migrations

python3 manage.py migrate
Create a superuser (admin account)

python3 manage.py createsuperuser
Load sample data (optional)

python3 manage.py loaddata programs/fixtures/sample_data.json
Run the development server

python3 manage.py runserver
Access the application

Main site: http://127.0.0.1:8000/
Admin panel: http://127.0.0.1:8000/admin/
Usage
For Students
Register for an account via the signup page
Browse available courses and instructors
View your personalized dashboard
Take tests and view results
Track your attempted tests
Report issues or problems
For Instructors/Admins
Log in to the admin panel
Create courses and associate with instructors
Add tests with multiple choice questions
Manage participants and enrollments
View student submissions and progress
Database Models
Course: Educational programs with title, description, and duration
Instructor: Instructor profiles with bio and video introduction
Participant: Course participants with contact information
Test: Assessments associated with courses
Question: Test questions with multiple choices
Choice: Answer options with correct answer marking
StudentSubmission: Student test attempts and scores
StudentProfile: User profiles with registration numbers
ProblemReport: Issue reporting system
Configuration
Key settings in Project/settings.py:

SECRET_KEY: Change for production deployment
DEBUG: Set to False in production
ALLOWED_HOSTS: Add your domain names
DATABASES: Configure your database
STATIC_ROOT: Static files collection directory
Security Notes
⚠️ Before deploying to production:

Change the SECRET_KEY in settings.py
Set DEBUG = False
Configure ALLOWED_HOSTS properly
Use a production-grade database (PostgreSQL, MySQL)
Set up proper static file serving
Enable HTTPS
Configure environment variables for sensitive data
Available Fixtures
Load sample data for testing:

demo_full.json - Complete sample dataset
demo_tests.json - Sample tests and questions
sample_data.json - Basic sample data
Contributing
Fork the repository
Create a feature branch (git checkout -b feature/YourFeature)
Commit your changes (git commit -m 'Add some feature')
Push to the branch (git push origin feature/YourFeature)
Open a Pull Request
License
This project is open source and available for educational purposes.

Author
Suryansh Kumar Rai

GitHub: @suryanshukumarrai
Acknowledgments
Built with Django Framework
Bootstrap for responsive design
Django community for excellent documentation
For questions or support, please open an issue on GitHub.
