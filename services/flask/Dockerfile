FROM python:3.9-slim

ENV FLAG=flag{}

WORKDIR /app

COPY ./requirements.txt /app/

RUN pip install --trusted-host pypi.python.org -r requirements.txt

COPY . /app

EXPOSE 8000

ENTRYPOINT ["gunicorn", "-t", "60", "-w", "4", "-b", "0.0.0.0:8000", "app:app"]
