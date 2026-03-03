FROM python:3.12-slim

COPY app.py .

WORKDIR /app

RUN apt-get update && \
    apt-get install -y curl && \
    pip install --no-cache-dir flask


EXPOSE 8080

CMD ["python", "app.py"]