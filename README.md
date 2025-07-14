# Running Multiple Containers with Docker Compose
This shows the process of running multiple containers with Docker Compose, which will run a website app.
Two images are used: a MySQL base image and an image built using a Dockerfile that runs a Python script.
The Docker Compose file sets required environment variables and exposes the necessary ports for each container.

## Steps to run:
Build and run containers
```
docker-compose up --build
```
As the Docker Compose file states, it will build an image from the current directory, looking for a Dockerfile. The "web" container is dependent on the "db" container; therefore, it controls the start order.
The app can be accessed in a browser with http://localhost:5000
