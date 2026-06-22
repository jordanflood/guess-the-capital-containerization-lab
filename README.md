# coding-project-template

# IBM Containerized Quiz Application

A simple static quiz web application containerized using Docker and served with Nginx.

This project was completed as part of my IBM cloud/containerization coursework and added to my portfolio as evidence of hands-on practice with Docker, containers, and basic cloud-native application workflows.

## Project Overview

The application is a browser-based quiz app that displays capital city questions. The static files are served through an Nginx web server inside a Docker container.

## Skills Practiced

* Creating a Dockerfile
* Using an official Docker base image
* Containerizing a static web application
* Serving frontend files with Nginx
* Building and running Docker images locally
* Mapping container ports
* Testing a containerized application in the browser
* Documenting technical work for a portfolio

## Technologies Used

* Docker
* Nginx
* HTML
* CSS
* JavaScript
* JSON
* Git
* GitHub

## Project Files

* `Dockerfile` - defines the container image
* `index.html` - main application page
* `style.css` - application styling
* `script.js` - quiz logic
* `data.json` - quiz data
* `favicon.ico` - browser icon

## How to Run

Build the Docker image:

```bash
docker build -t guess-the-capital .
```

Run the container:

```bash
docker run -p 8080:80 guess-the-capital
```

Open the application in the browser using port `8080`.

## What I Learned

Through this lab, I learned how a static web application can be packaged into a Docker image and served through Nginx.

I also learned that the container runs Nginx on port `80`, while the application can be accessed from outside the container by mapping it to another port, such as `8080`.

## Course Context

This project was completed as part of IBM cloud/containerization coursework.

The original starter project was provided by IBM Developer Skills Network. This repository is used for personal learning documentation and portfolio evidence.
