FROM python:3.9-slim

# Create a user `vscode`
RUN useradd -ms /bin/bash vscode

# Set the working directory
WORKDIR /app

# Copy the requirements and install dependencies
COPY flask-app/requirements.txt .
RUN pip install -r requirements.txt

# Copy the rest of the applicationFROM python:3.9-slim

# Set working directory
WORKDIR /workspace

# Copy requirements first to leverage Docker cache
COPY requirements.txt .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application
COPY . .

# Expose the port the app runs on
EXPOSE 5000

# Default command (can be overridden in docker-compose)
CMD ["flask", "run", "--host=0.0.0.0"]