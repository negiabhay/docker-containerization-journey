# Module 3 — Docker Containers

## Running containers

\`\`\`bash
docker run -d -p 5000:5000 --name my-flask-app flask-demo:1.0
\`\`\`

- `-d` — detached mode (runs in background, returns terminal control)
- `-p 5000:5000` — maps host port 5000 to container port 5000
- `--name` — gives the container a readable name instead of a random ID

## Detached vs interactive mode

- **Detached (`-d`)** — container runs in the background; used for
  long-running services like web servers.
- **Interactive (`-it`)** — attaches your terminal directly to the
  container; used for debugging or exploring inside a container.

\`\`\`bash
docker run -it ubuntu bash
\`\`\`

## Container lifecycle

\`\`\`bash
docker ps                  # list running containers
docker ps -a               # list all containers (including stopped)
docker stop my-flask-app   # stop a running container
docker start my-flask-app  # start a stopped container
docker rm my-flask-app     # remove a container
\`\`\`

## Logs and exec

\`\`\`bash
docker logs my-flask-app          # view container's stdout/stderr
docker exec -it my-flask-app bash # open a shell inside a running container
\`\`\`

## What I learned

`docker exec` only works on a **running** container — useful for live
debugging without stopping the service. `docker logs` was the first place
I'd check when a container exits immediately after starting.
