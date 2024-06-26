FROM ubuntu:22.04

RUN apt-get update && apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Install Flask using pip3
RUN pip3 install Flask

# Create a directory for the app
RUN mkdir -p /app

# Set the working directory
WORKDIR /app

# Copy the Flask app code into the container
COPY app.py /app

# Set the environment variable to tell Flask to run in container
ENV FLASK_APP=app.py

# Expose the port that the Flask app will run on
EXPOSE 5252

# Run the Flask app
CMD ["flask", "run", "--host=0.0.0.0", "--port=5252"]
