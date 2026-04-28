# Use the latest Ubuntu base image
FROM ubuntu:latest

# Update and upgrade APT
RUN apt-get update && apt-get upgrade -y

# Install python3 and python3-pip
RUN apt-get install -y python3 python3-pip

# Fix for "externally managed environment" error in newer Ubuntu/Python versions
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask using pip3
RUN pip3 install flask

# Set the working directory to /app
WORKDIR /app

# Copy api.py from your host machine to the /app directory in the container
COPY api.py /app/api.py

# Run the Flask app when the container starts
CMD ["python3", "api.py"]
