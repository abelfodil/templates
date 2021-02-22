FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu-20.04

RUN apt update \
    && apt install -y texlive-full \
    && apt-get autoremove -y && apt-get clean -y && rm -rf /var/lib/apt/lists/*
