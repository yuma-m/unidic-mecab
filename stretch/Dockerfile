FROM debian:stretch-slim

RUN apt-get update && \
    apt-get install -y mecab unidic-mecab python-mecab && \
    rm -rf /var/lib/apt/lists/*
