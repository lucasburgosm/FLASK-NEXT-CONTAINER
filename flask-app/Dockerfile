# [Choice] Debian version (use bullseye on local arm64/Apple Silicon): bullseye, buster
ARG VARIANT=bullseye
FROM mcr.microsoft.com/vscode/devcontainers/base:${VARIANT}

WORKDIR /workspace

RUN apt-get update && apt-get install -y \
    software-properties-common