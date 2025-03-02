ARG UV_VERSION="0.6.3"
# ref: variant list https://mcr.microsoft.com/v2/devcontainers/base/tags/list
ARG VARIANT="1.2.3-ubuntu24.04" 
FROM ghcr.io/astral-sh/uv:${UV_VERSION} as uv_source
FROM mcr.microsoft.com/vscode/devcontainers/base:${VARIANT}

RUN apt update && apt install -y \
    bash-completion \
    dnsutils \
    wget \
    ca-certificates

# install uv
COPY --from=uv_source /uv /uvx /bin/
RUN echo 'eval "$(uv generate-shell-completion bash)"' >> ~vscode/.bashrc