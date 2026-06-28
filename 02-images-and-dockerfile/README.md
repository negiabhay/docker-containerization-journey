# Module 2 — Docker Images & Dockerfile

## What is a Docker image
A blueprint for a container — a read-only template containing the app code,
dependencies, and instructions for how to run it. A container is a running
instance of an image.

## Dockerfile instructions used here

- `FROM python:3.11-slim` — base image to build on top of
- `WORKDIR /app` — sets the working directory inside the container
- `COPY` — copies files from the host into the image
- `RUN` — executes a command at build time (installing dependencies)
- `EXPOSE 5000` — documents which port the container listens on
- `CMD` — the command that runs when the container starts

## Hands-on — build and run

\`\`\`bash
docker build -t flask-demo:1.0 .
docker run -p 5000:5000 flask-demo:1.0
\`\`\`

Visit `http://localhost:5000` — should show the Flask response.

## What I learned

- `RUN` happens at **build time** (bakes into the image), `CMD` happens at
  **container start time**.
- Order of Dockerfile instructions matters for build caching — copying
  `requirements.txt` before the rest of the app code means Docker doesn't
  reinstall dependencies every time app code changes.
