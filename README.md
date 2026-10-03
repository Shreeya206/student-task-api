# Student Task API

A simple REST API for managing student tasks, built using Python Flask and containerized with Docker.

## Project Overview

This project demonstrates a basic client-server application packaged inside a Docker container.

The API allows users to:

- View all tasks
- Add a new task
- Check the health of the application

## Technologies Used

- Python
- Flask
- Docker
- Git
- GitHub
- AWS EC2

## Architecture

Client → AWS EC2 Instance → Docker Container → Flask REST API → Student Tasks

## API Endpoints

### Home

GET /

Returns a message confirming that the API is running.

### Health Check

GET /health

Returns the health status of the API.

### Get Tasks

GET /tasks

Returns the list of available tasks.

### Add Task

POST /tasks

Adds a new task to the task list.

Example request:

{ "title": "Learn Docker" }

## Run Locally Without Docker

Install the dependencies:

python -m pip install -r requirements.txt

Run the application:

python app.py

Open in your browser:

http://localhost:5000

## Run Using Docker

Build the Docker image:

docker build -t student-task-api .

Run the container:

docker run -d -p 5000:5000 --name student-task-api-container student-task-api

Open in your browser:

http://localhost:5000

## Deployment

The application is intended to be deployed on an AWS EC2 instance using Docker.

## Project Status

The application has been tested locally using Flask and Docker.

