ARG VARIANT="bookworm"
FROM mcr.microsoft.com/devcontainers/base:${VARIANT}

USER root

RUN export DEBIAN_FRONTEND=noninteractive && \
    apt-get update && \
    apt-get install -y wget && \
    wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg && \
    echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list && \
    apt-get update && \
    apt-get -y install --no-install-recommends \
        vagrant && \
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
