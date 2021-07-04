FROM python:3.9-slim-buster
WORKDIR /app
COPY requirements.txt /app
RUN python -m pip install -r requirements.txt
COPY . /app
EXPOSE 5000
ENTRYPOINT [ "gunicorn", "--workers=3", "--bind", "0.0.0.0:5000", "app:app" ]