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

# Docker build command: docker build -t docker_example_1 .
# Docker run command: docker run -d -p 5001:5000 docker_example_1