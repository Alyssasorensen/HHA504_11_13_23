FROM python:3.10-slim-buster
WORKDIR /app
COPY . /app/
RUN pip install -r requirements.txt
EXPOSE 5000
CMD ["python", "flaskapp.py"]

# Docker build command: docker build -t flask1
# Docker run command: docker run -d -p 5001:5000 flask2