# [Choice] Debian version (use bullseye on local arm64/Apple Silicon): bullseye, buster
ARG VARIANT=bullseye
FROM mcr.microsoft.com/vscode/devcontainers/base:${VARIANT}

WORKDIR /workspace

RUN apt-get update && apt-get install -y \
    software-properties-common \
    python3 \
    python3-pip \
    python3-dev \
    && rm -rf /var/lib/apt/lists/*

# Install additional Python dependencies
COPY requirements.txt /workspace/
RUN pip3 install --no-cache-dir -r requirements.txt

# Expose the port Flask will run on
EXPOSE 5000

# Run your application or start any other service you need
CMD ["flask", "run", "--host=0.0.0.0", "--port=5000"]