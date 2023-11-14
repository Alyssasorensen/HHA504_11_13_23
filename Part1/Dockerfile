# This command sets the base image for the Docker image to be built. In this case, it uses the official Python 3.7 image based on Alpine Linux.
FROM python:3.7-alpine
# This command sets the working directory within the container to '/app.' All subsequent commands will be executed in this directory.
WORKDIR /app
# This command copies the contents of the current directory (where the Dockerfile is located) into the '/app' directory in the container.
COPY . /app
# This command installs the Python dependencies specified in the 'requirements.txt' file. 
RUN pip install -r requirements.txt
# This command informs Docker that the container will listen on port 5000 at runtime.
EXPOSE 5000
# This command specifies the default command to be executed when the container starts.
CMD ["python", "flaskapp.py"]

# Documentation 

# This step ensures that you are in the correct directory where your Dockerfile is located. 
# 1st Step: "cd" into the proper directory.

# The command docker build -t alyssa17 . initiates the process of building a Docker image. The -t flag allows you to specify a name (in this case, "alyssa17") and optionally a tag for the image. The dot . at the end of the command indicates that the build context is the current directory.
# 2nd Step: then insert the following command, "docker build -t alyssa17 .," alyssa17 is the name I decided to use.

# After building the image, the command docker images is used to list all the Docker images present on your system.
# 3rd Step: once that finishes, I insert the command, "docker images," and I am able to see the repository "alyssa17."

# The command docker run -d -p 5001:5000 alyssa17 runs a Docker container based on the "alyssa17" image. The -d flag runs the container in detached mode, and the -p flag maps port 5001 on the host to port 5000 on the container. 
# 4th Step: then insert the following command, "docker run -d -p 5001:5000 alyssa17."

# Finally, the command docker ps lists all the currently running Docker containers. Verifying the presence of the "alyssa17" image in the list confirms that the container is up and running. 
# 5th Step: then insert the command, "docker ps," and the image "alyssa17" will appear. 


# Docker build command: docker build -t docker_example_1 .
# Docker run command: docker run -d -p 5001:5000 docker_example_1

# Experienced no challenges 