# Use the base image with the required Debian version
ARG VARIANT=bullseye
FROM mcr.microsoft.com/vscode/devcontainers/base:${VARIANT}

# Set working directory to /workspace
WORKDIR /workspace

# Install Python and pip
RUN apt-get update && apt-get install -y \
    python3 \
    python3-pip \
    && apt-get clean

# Set default Python version to python3
RUN update-alternatives --install /usr/bin/python python /usr/bin/python3 1

# Verify Python and pip installation
RUN python --version && pip3 --version
