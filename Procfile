release: . venv/bin/activate ; venv/bin/python manage.py makemigrations ; venv/bin/python manage.py migrate ; touch /tmp/app-initialized
web: cp bin/nginx/nginx.conf /tmp/nginx/conf/nginx.conf ; touch /tmp/nginx/logs/error.log ; bin/nginx ; venv/bin/gunicorn onlinechess.asgi:application -b=unix:/tmp/nginx.socket -k uvicorn.workers.UvicornWorker
