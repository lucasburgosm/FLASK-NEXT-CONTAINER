# [Choice] Debian version (use bullseye on local arm64/Apple Silicon): bullseye, buster
ARG VARIANT=bullseye
FROM mcr.microsoft.com/vscode/devcontainers/base:${VARIANT}

# Update package list and install necessary packages
RUN apt-get update && apt-get install -y \
    software-properties-common \
    npm \
    python3 \
    python3-pip \
    python3-dev \
    build-essential \
    curl \
    ca-certificates

# Ensure npm is the latest version and install 'n' for Node.js version management
RUN npm install npm@latest -g && \
    npm install -g n && \
    n latest

# Set working directory (optional)
WORKDIR /workspace

# Expose port (optional, adjust if needed)
EXPOSE 3000

# Default command (change based on your project needs)
CMD ["bash"]
