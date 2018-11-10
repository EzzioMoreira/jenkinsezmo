# Dockerfile Jenkins/container in container

Running jenkins with docker from host
To run the container, you need add a volume in docker run command.

… -v /var/run/docker.sock:/var/run/docker.sock …
It will share the docker socket (used in your machine) with the container.

The complete run command:

$ docker run --name jenkins-docker -p 8080:8080 -v /var/run/docker.sock:/var/run/docker.sock ezmo/jenkins
After inicialized the jenkins, complete the jenkins startup wizard.

Read this tutorial to complete wizard and install the locale and blueocean plugins: Quick start with jenkins in docker.
