# Backend-PHP-Symfony-Technical-Assignment
# Social Platform Backend (Django DRF)

Minimal runnable scaffold for the social backend focusing on:
- JWT auth (SimpleJWT)
- Users app (Profile, register, follow)
- Videos app (upload, like, view, search)
- Celery thumbnail task (requires ffmpeg or moviepy dependencies)

## Quick start (local, no Docker)
1. Python 3.10+ recommended.
2. Create venv and activate:
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```
3. Install requirements:
   ```bash
   pip install -r requirements.txt
   ```
4. Create `.env` from `.env.example` and adjust settings.
5. Run migrations:
   ```bash
   python manage.py migrate
   python manage.py createsuperuser
   ```
6. Run server:
   ```bash
   python manage.py runserver
   ```
7. Import `postman_collection.json` into Postman and set `{{base_url}}` to `http://localhost:8000`

## Using Docker Compose
```bash
docker-compose up --build
```

## Notes
- This is a scaffold. For production use, configure S3 for media, HTTPS, and proper secrets.
- Thumbnail generation requires `moviepy` and `ffmpeg` installed on the system.
