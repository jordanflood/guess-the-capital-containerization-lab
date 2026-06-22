# Learning Log: Guess the Capital Containerization Lab

## Context

This lab was completed as part of my IBM cloud and containerization coursework.

The purpose of the lab was to practice containerizing a simple static web application using Docker and serving it through Nginx.

## Objective

The objective was to take an existing static web application and package it into a Docker image so that it could be run consistently inside a container.

## Steps Completed

1. Cloned the starter project.
2. Reviewed the application files.
3. Ran the application locally using Python's HTTP server.
4. Confirmed the application worked in the browser.
5. Created a Dockerfile.
6. Used the official Nginx image as the base image.
7. Copied the static application files into the Nginx web directory.
8. Built a Docker image from the Dockerfile.
9. Ran the Docker container.
10. Mapped host port `8080` to container port `80`.
11. Opened and tested the containerized application in the browser.
12. Uploaded the completed lab project to GitHub as portfolio evidence.

## Key Commands Used

Run the application locally before containerization:

```bash
python3 -m http.server
```

Build the Docker image:

```bash
docker build -t guess-the-capital .
```

Run the container:

```bash
docker run -p 8080:80 guess-the-capital
```

Check running containers:

```bash
docker ps
```

## What I Learned

I learned that a Dockerfile is a set of instructions used to build a Docker image.

In this lab, the Dockerfile used Nginx as the base image. The static web application files were copied into Nginx's default web directory so that Nginx could serve the application from inside the container.

I also learned how Docker port mapping works. The application runs on port `80` inside the container, but I mapped it to port `8080` so it could be accessed from the browser.

## Problem Encountered

While testing the app locally, port `8000` was already in use. This happened because a Python HTTP server process was already running.

## How I Solved It

I stopped the running process and continued with the Docker-based version of the lab.

## Reflection

This lab helped me understand the basic containerization workflow used in cloud-native development.

The most useful part was seeing how a simple application can be packaged with its runtime environment, then run consistently as a container. This is directly relevant to cloud, DevOps, QA, and platform engineering work because containers are commonly used to deploy and test applications in repeatable environments.
