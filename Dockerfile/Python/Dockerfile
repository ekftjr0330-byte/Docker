FROM python:3.14-alpine
WORKDIR /app
COPY app.py .
RUN apt-get install -y curl 
RUN pip install --no-cache-dir flask
EXPOSE 8080
CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0", "--port=8080"]
