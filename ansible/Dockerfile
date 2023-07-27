FROM python:3.9.17-slim

# Keeps Python from generating .pyc files in the container 
ENV PYTHONDONTWRITEBYTECODE=1 
 
# Turns off buffering for easier container logging 
ENV PYTHONUNBUFFERED=1 

RUN apt-get update && apt-get install -y git

WORKDIR /usr/src/app

COPY requirements.txt .

RUN pip install --upgrade pip setuptools && \
    pip install -r requirements.txt

# User for vscode
RUN adduser -u 5678 --disabled-password --gecos "" vscode
