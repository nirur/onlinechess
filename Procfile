release: . venv/bin/activate ; venv/bin/python manage.py makemigrations ; venv/bin/python manage.py migrate ; touch /tmp/app-initialized
web: bin/start-nginx venv/bin/gunicorn -c conf/gunicorn.conf.py 'onlinechess.asgi:application' -k uvicorn.workers.UvicornWorker
