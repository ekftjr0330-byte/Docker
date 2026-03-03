FROM python:3.12-slim

WORKDIR /app

COPY app.py .

RUN apt-get update && \
    apt-get install -y curl && \
    apt-get clean

RUN pip install --no-cache-dir flask

EXPOSE 8080

CMD ["python", "app.py"]
