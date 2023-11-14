# Docker_Flask_Homework
## HHA 504 Assignment 8
This task is designed to offer practical exposure to the process of containerizing Flask applications using Docker, initially on an individual basis and subsequently utilizing Docker Compose to oversee multiple applications.

**The Process of Dockerizing the Applications in Both Parts**
1. Create a Flask Application:

Develop your Flask application if you haven't already. Ensure that it has a requirements.txt file listing all the Python dependencies needed to run the application.

2. Write a Dockerfile:

Create a file named Dockerfile in the root of your project. This file contains instructions for building the Docker image.

```
# Use an official Python runtime as a parent image
FROM python:3.10-slim

# Set the working directory to /app
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# Make port 5000 available to the world outside this container
EXPOSE 5000

# Define environment variable
ENV NAME World

# Run app.py when the container launches
CMD ["python", "app.py"]
```

Modify this file based on your project structure and requirements.

4. Build the Docker Image:

Open a terminal in the project directory and run the following command to build the Docker image. The dot at the end signifies the build context.

```
docker build -t your_image_name .
```

Replace "your_image_name" with the desired name for your Docker image.

4. Run the Docker Container:

Once the image is built, you can run a container based on that image:

```
docker run -p 5000:5000 your_image_name
```

This command maps port 5000 on your local machine to port 5000 in the container. Adjust the ports as needed.

5. Access the Application:

Open a web browser and navigate to http://localhost:5000 to see your Flask application running inside the Docker container.

6. Use Docker Compose for Multi-Container Setup:

If your application has multiple services (e.g., a Flask app and a database), you can use Docker Compose to define and run a multi-container setup. Create a "docker-compose.yml" file and define your services, networks, and volumes.

```
version: '3'

services:
  web:
    build: .
    ports:
      - "5000:5000"
```

Run the application using:

```
docker-compose up
```

**The Build and Run Commands Used**

This is located in each of the files above. 

**Observations, challenges faced, and reflections on the use of Docker and Docker Compose**

Observations and challenges are located in the files above. 

**Docker:**

Isolation and Portability:

Docker enables the encapsulation of applications and their dependencies into containers. This isolation ensures consistency across different environments, making it easy to develop and deploy applications reliably.


**Docker Compose:**

Application Orchestration:

Docker Compose simplifies the management of multi-container applications by defining services, networks, and volumes in a single YAML file. This orchestration ensures that all components of the application are configured and run together.
