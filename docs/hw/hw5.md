# Homework assignment HW5

## Homework log

Remember to create a new post with a new topic "HW5" in your homework log channel on Microsoft Teams. Make a reply to that topic whenever do some work on this assignment. You can also post questions there. Your posts should provide evidence that you spent several hours doing meaningful work.

## Objectives

This assignment is designed to give you some experience with Docker, a popular containerization platform. You will learn how to install Docker, build a simple web server image, and run it in a container. As a preliminary to installing Docker on your Linux machine, you will install and run a web server on your Linux machine.

### Minimal knowledge and experience to acquire:
#### 1. Install and run a web server on your Linux machine.
* install `apache2` on on your Linux system
* launch apache web server: `sudo /etc/init.d/apache2 start`
* Configure the web server so that you can visit its default page (see e.g. the [Apache on GCP](../resources/apache_gcp_quickstart.md) page).
* Edit the default page at `/var/www/html/index.html`. Don't edit the file as root user. Practice adding yourself to a group that has write access to the file, and then edit it as a normal user. 
  - Commands similar to the following should work. Make sure you understand them all:
    ```bash
        sudo groupadd www
        sudo usermod -a -G www yourusername
        cd /var/www
        sudo chgrp -R www html
        sudo chmod -R g+w html
    ```
  - The Linux machine probably needs a reboot so that the new group permissions work correctly.

#### 2. Install Docker Engine (not Docker Desktop) on the Linux box, and run a simple web server in a Docker container.
* see e.g. [Install using the convenience script](https://docs.docker.com/engine/install/debian/#install-using-the-convenience-script)
* Verify Docker installation by running `docker run hello-world`
* Build a Docker image that runs a simple web server (e.g. `nginx` or `httpd`) and serves a simple HTML page. You can use the following Dockerfile as a starting point:
    ```dockerfile
    FROM nginx:alpine
    COPY index.html /usr/share/nginx/html/index.html
    ```
  - Create an `index.html` file with some content of your choice.
  - Build the image using `docker build -t my-web-server .`
  - Run the container using `docker run -d -p 8080:80 my-web-server`
  - Verify that you can access the web page at `http://localhost:8080` or `http://<your-linux-box-ip>:8080`
    * e.g., `curl http://localhost:8080` or `curl http://<your-linux-box-ip>:8080`
* practice using `docker ps`, `docker stop`, `docker start`, and `docker rm` commands to manage your container; also `docker images` and `docker rmi` to manage your images; `docker inspect` to inspect your container and image, e.g. `docker inspect <container name> | grep IPAddress`

#### 3. Be familiar with the differences between a virtual machine, a Docker image, a Docker container, and a Dockerfile.

## PB version

The Professor Braught version is available as:
* [05-A-Docker.docx](../materials/05-A-Docker.docx)
_Unless you already have familiarity with the above commands, it is a good idea to follow the PB version closely for this assignment._


## Likely quiz questions

* What is the difference between a container and a virtual machine?
* What is the difference between a Docker image and a Docker container?
* What is the difference between a Dockerfile and a Docker image?
* Explain each of the following Linux terminal commands:
  ```bash
  sudo groupadd www
  sudo usermod -a -G www yourusername
  sudo chgrp -R www html
  sudo chmod -R g+w html
  ```
  