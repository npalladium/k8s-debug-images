FROM bitnami/minideb:bullseye

RUN install_packages \
    ca-certificates \
    jq \
    procps psmisc \
    inetutils-ping dnsutils curl wget \
    tcpdump traceroute netcat openssl \
    python3 python3-pip \
    kubernetes-client

RUN python3 -m pip install --no-cache-dir pgcli --only-binary psycopg2
RUN curl https://downloads.mongodb.com/compass/mongodb-mongosh_1.4.1_amd64.deb -o mongodb-mongosh_1.4.1_amd64.deb && \
    dpkg -i mongodb-mongosh_1.4.1_amd64.deb && \
    rm mongodb-mongosh_1.4.1_amd64.deb
