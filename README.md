# Docker Containerization Journey

A structured, hands-on walkthrough of Docker — from fundamentals to a fully
automated CI/CD pipeline that builds, tests, pushes, and deploys a
containerized app to a live EC2 instance.

This repo is intentionally organized by topic so each concept is easy to
review on its own, rather than buried inside a single pipeline project.

## Why this repo exists

Most of my Docker usage lives inside CI/CD pipelines, where Docker is just
one step among many. This repo isolates and demonstrates the underlying
Docker fundamentals on their own — containers, images, volumes, networking,
and Compose — before tying everything together in a real deployment project.

## Modules

| Module | Topic | What it demonstrates |
|---|---|---|
| [01](./01-fundamentals) | Docker Fundamentals | Containers vs VMs, Docker architecture |
| [02](./02-images-and-dockerfile) | Images & Dockerfile | Writing a Dockerfile, building/tagging images |
| [03](./03-containers-lifecycle) | Container Lifecycle | Running, stopping, exec, logs |
| [04](./04-volumes) | Volumes | Persisting data across container restarts |
| [05](./05-networking) | Networking | Bridge networks, container-to-container communication |
| [06](./06-docker-compose) | Docker Compose | Multi-container app: Flask + PostgreSQL |
| [07](./07-docker-registry) | Docker Registry | Pushing/pulling images via Docker Hub |
| [08](./08-end-to-end-project) | **End-to-End Project** | Full CI/CD pipeline: build → test → push → deploy to EC2 |

## Tech stack

- Docker & Docker Compose
- Flask (Python)
- PostgreSQL
- GitHub Actions
- AWS EC2
- Docker Hub

## Related projects

- [`payeasy-cicd-project`](https://github.com/negiabhay/payeasy-cicd-project) — CI/CD pipeline with matrix testing, artifacts, and EC2 deployment via appleboy SSH action
- [`bash-scripting-for-devops`](https://github.com/negiabhay/bash-scripting-for-devops) — AWS CLI scripting practice
