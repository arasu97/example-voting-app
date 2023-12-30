
FROM python:3.11
ADD . .
RUN apt-get update 
RUN install watchdog
CMD ["python", "app.py"]
EXPOSE 80
CMD ["gunicorn", "app:app", "-b", "0.0.0.0:80", "--log-file", "-", "--access-logfile", "-", "--workers", "4", "--keep-alive", "0"]
