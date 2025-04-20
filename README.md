## Running the Project

Before you start, make sure you have:

- Python 3.x and your virtual environment activated  
- Redis installed (e.g. via Homebrew on macOS or your system’s package manager)  
- Daphne, Celery, and other dependencies installed:
  ```bash
  pip install -r requirements.txt

Start the ASGI server:
  daphne my_project.asgi:application

Start Redis:
  - macOS (Homebrew):
brew services start redis

Start Celery (worker + beat scheduler):
  celery -A my_project worker -B --loglevel=info

Once all three are running, your application will be available at:
  http://127.0.0.1:8000


Python version: 3.13.2
Celery version: 5.5.1 (immunity)
Django version: 5.1.5
