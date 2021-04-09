# Video-Blog - Docker
Video-Blog is an application built in React that renders a youtube video. This application is designed to be containerized with the use of Docker. 

Docker is a open-source platform designed to make it easier to create, deploy, and run applications by using containers. 

A container runs an instance of an image. An image is the application, video-blog, packaged up along with it's dependencies and the environment needed to run. 

The image for video-blog is built using a Dockerfile, which is then used in a ```docker-compose.yaml``` file to deploy. 

## How to Run
Run video-blog locally: 

- Clone this repository
- Navigate to the project. In a terminal run ```npm install && npm start```
- The application is available at http://localhost:3000/

Run video-blog using Docker:

- Clone this repository
- Navigate to the project. In a terminal run ```docker-compose up -d ```
- The application is available at http://localhost:3000/

## Cleardown
Once you deploy video-blog locally, run ```sh cleardown.sh``` in a terminal and all images and containers will be removed/deleted. 

## Container Registry
A container registry is a central place to store, host and distribute container images. A container registry is better suited for a development/production workflow i.e. anything other than running applications locally. I use AWS ECR to store my images and have built a script, ```dockerbuildpushawsecr.sh```, that builds, tags and pushes images to an AWS ECR repository.
