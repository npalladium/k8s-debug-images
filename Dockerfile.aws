FROM bitnami/minideb:bullseye

RUN install_packages \
    ca-certificates zip unzip gzip jq procps tar build-essential \
    inetutils-ping dnsutils curl wget \
    python3 python3-pip python3-venv python3-setuptools python3-dev \
    postgresql-client libpq-dev \
    kubernetes-client

RUN python3 -m pip install pipx && python3 -m pipx ensurepath
RUN python3 -m pipx install pgcli
ENV AWS_PAGER=""
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && unzip -q awscliv2.zip && ./aws/install && rm -rf awscliv2.zip
