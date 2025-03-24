FROM debian:bullseye-slim

WORKDIR /workspace

RUN apt-get update && apt-get install -y \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

CMD ["sleep", "infinity"]