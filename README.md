# AWS Cloud & Docker-Based Portfolio Website

## About the Project

I built this portfolio website to showcase my skills, projects, and technical knowledge.

After developing the website locally using HTML, CSS, and JavaScript, I containerized it using Docker and deployed it on an AWS EC2 instance.

This project helped me get hands-on experience with Git, GitHub, Docker, Linux, and AWS EC2, along with the basic process of deploying a web application on the cloud.

## Project Flow

**Local Development → GitHub → Docker → AWS EC2 → Live Website**

## Architecture & Deployment Workflow

The application was developed and tested locally before deploying it to AWS.

### Deployment Flow

Local Portfolio Website
        ↓
      Git
        ↓
     GitHub
        ↓
   AWS EC2 Instance
        ↓
      Docker
        ↓
  Docker Container
        ↓
   Nginx Web Server
        ↓
   Live Website


### Deployment Process

1. I created and tested the portfolio website on my local system.
2. I created a Git repository and pushed the project files to GitHub.
3. I launched an AWS EC2 instance for hosting the application.
4. I connected to the EC2 instance using SSH.
5. I installed and configured Docker on the EC2 instance.
6. I cloned the GitHub repository into the EC2 instance.
7. I built a Docker image using the project's Dockerfile.
8. I created and started a Docker container from the image.
9. I configured the required port in the EC2 Security Group.
10. I accessed the deployed portfolio website using the EC2 public IP address.


## Technologies Used

* HTML
* CSS
* JavaScript
* Git
* GitHub
* Docker
* Nginx
* AWS EC2
* Linux

## What I Practiced

Through this project, I practiced:

* Creating and managing a GitHub repository
* Writing a Dockerfile
* Building a Docker image
* Running and managing Docker containers
* Working with Docker port mapping
* Connecting to an AWS EC2 instance using SSH
* Deploying a Dockerized application on EC2
* Configuring an AWS Security Group
* Accessing the deployed website using the EC2 public IP

## Docker Implementation

### Dockerfile

The application is served using Nginx inside a Docker container. A Dockerfile was created to build the Docker image and copy the website files into the Nginx web root directory.

FROM nginx:latest

COPY . /usr/share/nginx/html

### Build Docker Image


docker build -t portfolio-website .


### Run Docker Container


docker run -d -p 8080:80 --name portfolio-container portfolio-website


### Verify Container


docker ps
docker logs portfolio-container


## AWS EC2 Deployment

The Dockerized portfolio application was deployed on an AWS EC2 instance.

The EC2 instance was accessed through SSH, and the GitHub repository was cloned into the instance. Docker was then used to build the image and run the application container.

The application was accessed using the public IP address of the EC2 instance.

## Security Group Configuration

The EC2 Security Group was configured to allow the required inbound traffic for accessing the deployed web application.

## Troubleshooting

During the deployment, I practiced checking Docker container status and logs to identify and resolve issues.

Commands such as `docker ps`, `docker ps -a`, and `docker logs` were used for troubleshooting.

## What I Learned


This project helped me understand how the different tools and services work together to deploy an application.

I gained practical confidence in working with Linux, Git, Docker, and AWS EC2, and understood the basic workflow of moving an application from local development to a live cloud environment.

It also helped me improve my understanding of container-based deployment and basic troubleshooting while working on a real project.


## Project Outcome

The portfolio website was successfully containerized with Docker and deployed on an AWS EC2 instance.

This project gave me practical experience in taking an application from local development to a live cloud environment.
