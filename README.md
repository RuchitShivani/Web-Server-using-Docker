# Custom Web Server using Docker

## Overview
This project sets up a simple web server using Nginx inside a Docker container. The web server serves a custom frontend and is configured using a custom Nginx configuration file.

## Project Structure
```
custom-webapp/
│-- my-frontend/        # Contains frontend files (index.html, theme.css)
│-- server-config/      # Contains custom Nginx configuration (app.conf)
│-- Dockerfile          # Dockerfile to build the web server image
│-- .dockerignore       # Files to ignore in the Docker build process
```

## Prerequisites
- [Docker](https://docs.docker.com/get-docker/) installed on your system

## Installation & Usage
### 1. Clone the Repository
```sh
git clone https://github.com/your-username/custom-webapp.git
cd custom-webapp
```

### 2. Build the Docker Image
```sh
docker build -t my-custom-webapp .
```

### 3. Run the Docker Container
```sh
docker run -d -p 7070:8181 --name my-web-container my-custom-webapp
```

### 4. Access the Web Server
Once the container is running, open your browser and go to:
```
http://localhost:7070
```

## Managing the Container
### Stop the container
```sh
docker stop my-web-container
```

### Restart the container
```sh
docker start my-web-container
```

### Remove the container
```sh
docker rm -f my-web-container
```

### Rebuild and restart (if you make changes)
```sh
docker build -t my-custom-webapp .
docker rm -f my-web-container
docker run -d -p 7070:8181 --name my-web-container my-custom-webapp
```

## Customization
Modify the frontend files in `my-frontend/` to update the website. 
Modify `server-config/app.conf` to change Nginx settings.

## License
This project is open-source. Feel free to modify and use it!

![Screenshot 2025-03-13 151756](https://github.com/user-attachments/assets/4deb29e6-e45a-4f35-9383-d67f218b28c8)
![Screenshot 2025-03-13 151750](https://github.com/user-attachments/assets/1cf092b0-878d-431f-9fa4-7abd0e0609b7)
![Screenshot 2025-03-13 151741](https://github.com/user-attachments/assets/05e940e1-200c-4d83-a09e-4b491430ac7d)
![Screenshot 2025-03-13 151733](https://github.com/user-attachments/assets/af30b210-2ab2-44bf-8fec-e9f11d394d2e)
![Screenshot 2025-03-13 151718](https://github.com/user-attachments/assets/9635b18c-f47d-4bd9-b799-9a28242383f3)
![Screenshot 2025-03-19 084515](https://github.com/user-attachments/assets/575375b1-8007-4642-b4d4-bbd609ea84ad)
![Screenshot 2025-03-19 084504](https://github.com/user-attachments/assets/573e5914-4702-40b1-bf3b-1a11e305148f)
![Screenshot 2025-03-19 084447](https://github.com/user-attachments/assets/5fe003c8-00a3-4a42-bb55-5c43f73a9ec5)
![Screenshot 2025-03-13 180552](https://github.com/user-attachments/assets/1f98ac26-9092-4609-8eed-d6a470e6ce41)
