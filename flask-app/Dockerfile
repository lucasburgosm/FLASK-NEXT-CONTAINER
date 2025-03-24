# Use an official Python runtime as a parent image (e.g., Debian-based Python image)
FROM python:3.9-slim

# Set the working directory inside the container
WORKDIR /app

# Install any needed Python packages specified in requirements.txt
COPY flask-app/requirements.txt /app/requirements.txt
RUN pip install --no-cache-dir -r /app/requirements.txt

# Copy the entire project folder into the container's /app folder
COPY . /app

# Set environment variables for Flask
ENV FLASK_APP=app.py
ENV FLASK_ENV=development

# Expose port 5000 for Flask
EXPOSE 5000

# Run the Flask app
CMD ["flask", "run", "--host=0.0.0.0"]
