FROM python:alpine

WORKDIR /app

COPY requirements.txt /app

COPY devops /app

RUN apk update && \
    apk add --no-cache gcc musl-dev && \
    pip install --no-cache-dir -r requirements.txt && \
    cd devops

ENTRYPOINT ["python3"]
CMD ["manage.py", "runserver", "0.0.0.0:8000"]
