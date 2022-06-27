FROM bitnami/minideb:bullseye

RUN install_packages \
    ca-certificates build-essential \
    zip unzip gzip tar \
    jq \
    procps psmisc \
    inetutils-ping dnsutils curl wget \
    tcpdump traceroute netcat openssl \
    python3 python3-pip python3-venv python3-setuptools python3-dev \
    postgresql-client libpq-dev \
    kubernetes-client

RUN python3 -m pip install pipx && python3 -m pipx ensurepath
RUN python3 -m pipx install pgcli
RUN curl https://downloads.mongodb.com/compass/mongodb-mongosh_1.4.1_amd64.deb -o mongodb-mongosh_1.4.1_amd64.deb && dpkg -i mongodb-mongosh_1.4.1_amd64.deb
