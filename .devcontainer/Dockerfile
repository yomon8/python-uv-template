FROM ghcr.io/astral-sh/uv:0.5.31 AS uv

FROM mcr.microsoft.com/vscode/devcontainers/python:1-3.12-bookworm

RUN --mount=from=uv,source=/uv,target=/bin/uv \
    cp /bin/uv /usr/local/bin/uv

RUN apt update && apt install -y \
    bash-completion \
    dnsutils \
    wget \
    fzf \
    ca-certificates
