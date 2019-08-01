FROM ubuntu:16.04

WORKDIR /app
COPY . .
RUN apt-get update && apt-get install -y python wget && \
    apt install -y python3-pip ffmpeg && \
    pip3 install pycryptodome && \    
    pip3 install --user --upgrade yle-dl && \
    rm -rf /var/lib/apt/lists/*
ENTRYPOINT ["/root/.local/bin/yle-dl"]



