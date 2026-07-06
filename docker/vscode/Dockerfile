FROM lscr.io/linuxserver/code-server:latest

LABEL maintainer="Archit Awasthi"
LABEL project="Orbit"
LABEL description="Universal Development Environment"

USER root

RUN apt-get update && \
    apt-get install -y \
        g++ \
        gdb \
        make \
        cmake && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# Give the normal code-server user ownership again
RUN chown -R abc:abc /config

USER abc