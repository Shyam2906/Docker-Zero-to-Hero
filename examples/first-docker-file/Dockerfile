FROM python:3.9

WORKDIR /app

COPY requirements.txt /app
COPY devops /app

ENV PIP_BREAK_SYSTEM_PACKAGES 1

RUN pip install -r requirements.txt
Run python manage.py migrate

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]
