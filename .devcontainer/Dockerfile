FROM python:3.12-slim

# This is based on https://github.com/trr266/otree3_docker/blob/master/Dockerfile

WORKDIR /app

COPY requirements.txt .

RUN apt-get update && \
    apt-get install -y git && \
    pip install --upgrade pip && \
    pip install -r requirements.txt

COPY src /app/

CMD ["otree", "prodserver", "8000"]
