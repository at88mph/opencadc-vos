FROM python:3.5-slim

ARG VOS_PACKAGE=vos

RUN apt-get update \
    && apt-get install -y gcc git libc-dev libffi-dev libmagic-dev libssl-dev libxslt-dev make \
    && apt-get clean \
    && apt-get autoclean \
    && rm -rf /var/lib/apt/lists/*
  
RUN pip install --no-cache-dir ${VOS_PACKAGE}
