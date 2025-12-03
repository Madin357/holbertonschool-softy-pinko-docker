# Base image
FROM ubuntu:latest

# Update and upgrade packages
RUN apt-get update && apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Remove externally managed restriction if present
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Install Flask via pip3
RUN pip3 install flask

# Set working directory
WORKDIR /app

# Copy Flask app into container
COPY ./api.py /app/api.py

# Command to run the Flask app
CMD ["python3", "/app/api.py"]
