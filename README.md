# Student Task API

A simple REST API for managing student tasks, built using Python Flask and Docker and deployed on AWS EC2.

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

- GET `/` - Checks whether the API is running
- GET `/health` - Checks API health
- GET `/tasks` - Returns all tasks
- POST `/tasks` - Adds a new task

## Deployment

The application is deployed on an AWS EC2 instance using Docker.

Live API:

http://16.171.193.14:5000

Health Check:

http://16.171.193.14:5000/health

## Local Run

Install Flask:

`pip install flask`

Run the application:

`python app.py`

## Docker Run

Build the Docker image:

`docker build -t student-task-api .`

Run the container:

`docker run -d -p 5000:5000 --name student-task-api-container student-task-api`

## Project Status

The application has been tested locally using Flask and Docker and is currently deployed and running on AWS EC2.
