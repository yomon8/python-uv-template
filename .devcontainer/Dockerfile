FROM mcr.microsoft.com/vscode/devcontainers/python:1-3.12-bookworm

RUN apt update && apt install -y \
    bash-completion \
    dnsutils \
    wget \
    fzf \
    ca-certificates

RUN wget -qO- https://astral.sh/uv/install.sh | sh

ENV CARGO_HOME="/opt/.cargo/bin"
RUN mkdir -p $CARGO_HOME
RUN mv /root/.local/bin/uv /usr/local/bin/
