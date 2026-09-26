# Auth Microservice

A small FastAPI authentication service organized into a package-based project layout.

## Project structure

auth-microservice/
├── app/
│   ├── __init__.py
│   ├── auth.py
│   ├── database.py
│   ├── main.py
│   ├── models.py
│   └── schemas.py
├── .env
├── Dockerfile
├── README.md
├── main.py
├── requirements.txt
├── run.py
└── .gitignore

## Run the app

1. Install dependencies:
   pip install -r requirements.txt

2. Start the app:
   python run.py

3. Or use uvicorn directly:
   uvicorn app.main:app --reload

4. The default local database is SQLite for this environment, so no PostgreSQL driver is required.

## Notes

- The root-level files are kept as compatibility wrappers so older imports still work.
- The canonical application code lives inside the app package.

## Dependencies

- fastapi
- uvicorn
- sqlalchemy
- psycopg2-binary
- python-jose[cryptography]
- passlib[bcrypt]
- python-dotenv
