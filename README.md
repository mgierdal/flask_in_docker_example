# flask_in_docker_example

How to use Docker for development and for a simple way of distribution (borrowed from Gabor Szabo and other sources on internet).

[Flask in Docker Development](https://code-maven.com/flask-in-docker-development)

- web
- Dockerfile

[Containerized Python Development Part 1](https://www.docker.com/blog/containerized-python-development-part-1/)

- app
- Dockerfile_fat (single stage, ~ 900MB)
- Dockerfile_multistage (multi stage, <200MB)
- Dockerfile_ms2 (to be tested)

`sudo docker build -f Dockerfile_fat -t fat ./app`

`sudo docker run -p 5001:5000 fat`

or

`sudo docker build -f Dockerfile_multistage -t multistage ./app`

`sudo docker run -p 5000:80 multistage`
