release: . venv/bin/activate venv/bin/python manage.py migrate
web: venv/bin/gunicorn onlinechess.asgi:application -b=0.0.0.0:$PORT -k uvicorn.workers.UvicornWorker
