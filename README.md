Project Calibrations

Requirements: Python 3.12+ (recommended 3.14), Django 6.1, PostgreSQL

Instruction to use:
1. Setup a dir for project
2. $ git clone https://github.com/maciej88/calibration.git
3. navigate in to "calibration" dir
4. setup a venv (Windows: py -3.14 -m venv .venv):
   $ python3.14 -m venv .venv
5. activate venv and install requirements:
   $ pip install -r requirements.txt
6. make "calibration/.env" file (secret) with structure:
   SECRET_KEY='{here secret key as string}'
   DATABASE_URL='postgres://{user}:{password}@localhost:5432/{calibration}'
   (for local tests you can use: DATABASE_URL='sqlite:///db.sqlite3')
7. $ python manage.py makemigrations calib_management
8. $ python manage.py migrate
9. $ python manage.py runserver
