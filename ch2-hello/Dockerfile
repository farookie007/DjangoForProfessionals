# Pull base image
FROM python:3.10.4-slim-bullseye

# Set environment variables
ENV PIP_DISABLE_PIP_VERSION_CHECK 1
ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

# Set work directory => this sets `/code` as our working directory inside the docker image which subsequently allows relative path
WORKDIR /code

# Install dependencies => this copies the `requirements.txt` file in the local cwd into the image's cwd
COPY ./requirements.txt .
RUN pip install -r requirements.txt

# Copy project => copies every file and folders in the local cwd into the image's cwd
COPY . .
