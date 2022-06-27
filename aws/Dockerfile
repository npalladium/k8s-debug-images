FROM bitnami/minideb:bullseye

RUN install_packages \
    ca-certificates \
    zip unzip gzip tar \
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

ENV AWS_PAGER=""
RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && unzip -q awscliv2.zip && ./aws/install && rm -rf awscliv2.zip
