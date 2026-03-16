FROM python:3.11-slim AS builder
WORKDIR /app
RUN pip install --no-cache-dir --user Flask==2.3.3
FROM python:3.11-slim
WORKDIR /app
RUN mkdir -p /var/log/app && chmod 777 /var/log/app
COPY --from=builder /root/.local /root/.local
COPY app.py .
ENV PATH=/root/.local/bin:$PATH
ENV FLASK_APP=app.py
EXPOSE 5000
CMD ["flask", "run", "--host=0.0.0.0", "--port=5000"]