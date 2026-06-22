# Guess the Capital Containerization Lab

A simple static web application containerized using Docker and served with Nginx.

This project was completed as part of my IBM cloud and containerization coursework. I added it to my GitHub portfolio as evidence of hands-on practice with Docker, container images, port mapping, and basic cloud-native application workflows.

## Project Overview

This lab project takes a static browser-based web application and packages it into a Docker container. The application files are copied into the default Nginx web directory so they can be served by an Nginx web server inside the container.

## Skills Practiced

* Creating a Dockerfile
* Using an official Docker base image
* Containerizing a static web application
* Serving frontend files with Nginx
* Building Docker images locally
* Running Docker containers
* Mapping host ports to container ports
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
* `script.js` - client-side application logic
* `data.json` - application data
* `favicon.ico` - browser icon

## Dockerfile Summary

The Dockerfile uses the official Nginx image:

```dockerfile
FROM nginx
```

The application files are copied into:

```text
/usr/share/nginx/html/
```

This is the default directory Nginx uses to serve static web content.

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

I also learned the difference between the port inside the container and the port used to access the application externally. Nginx runs on port `80` inside the container, while Docker maps that to port `8080` on the host.

This helped me understand the basic workflow of containerizing an application:

1. Test the application locally.
2. Create a Dockerfile.
3. Build a Docker image.
4. Run the application as a container.
5. Access the containerized application through a mapped port.

## Course Context

This project was completed as part of IBM cloud/containerization coursework.

The original starter project was provided by IBM Developer Skills Network. This repository is used for personal learning documentation and portfolio evidence.

