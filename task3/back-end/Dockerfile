# Base Image
FROM ubuntu:latest

# Update APT
RUN apt-get update

# Upgrade
RUN apt-get upgrade -y

# Install python3, python3-pip, and flask
RUN apt-get install -y python3 python3-pip
RUN pip3 install flask
RUN pip3 install flask-cors

# Set working directory
WORKDIR /app

# Copy the Python file to the working directory
COPY api.py /app

# Expose port 5252
EXPOSE 5252

# Start the Flask server
CMD ["python3", "api.py"]
