# Module 1 — Docker Fundamentals

## What is Docker
Docker packages an application with everything it needs to run — code,
runtime, libraries, system tools — into a single unit called a container.
This guarantees the app behaves the same way on any machine.

## Containers vs Virtual Machines

| | Containers | Virtual Machines |
|---|---|---|
| OS | Share the host OS kernel | Each VM has its own full OS |
| Size | Lightweight (MBs) | Heavy (GBs) |
| Startup | Seconds | Minutes |
| Isolation | Process-level | Hardware-level (stronger) |

## Docker Architecture

- **Docker Client** — the CLI you type commands into (`docker run`, `docker build`)
- **Docker Daemon (dockerd)** — runs in the background, does the actual work of building/running containers
- **Docker Registry** — stores images (e.g. Docker Hub)

Flow: Client sends a command → Daemon executes it → pulls images from Registry if needed.

## First container — hands-on

\`\`\`bash
docker run hello-world
\`\`\`

This pulls the `hello-world` image (if not already local) from Docker Hub,
creates a container from it, runs it, and prints a confirmation message.
Confirms Docker is installed and working end to end.
