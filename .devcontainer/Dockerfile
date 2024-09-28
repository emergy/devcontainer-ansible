ARG VARIANT="bookworm"
FROM mcr.microsoft.com/devcontainers/base:bookworm

USER root

RUN apt-get update && \
    export DEBIAN_FRONTEND=noninteractive && \
    apt-get -y install --no-install-recommends \
        python3-pip && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    pip3 install --no-cache-dir --break-system-packages \
        ansible \
        ansible-lint \
        yamllint \
        molecule \
        'molecule-plugins[vagrant]' \
        'molecule-plugins[docker]' \
        'molecule-plugins[containers]' \
        argcomplete && \
    activate-global-python-argcomplete

USER vscode
