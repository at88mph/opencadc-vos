FROM python:3.12-slim as builder

RUN apt-get update \
    && apt-get install -y gcc git libc-dev libffi-dev libmagic-dev libssl-dev libxslt-dev make

FROM python:3.12-slim

ARG VOS_PACKAGE=vos

COPY --from=builder /usr/ /usr/
  
RUN pip install --no-cache-dir ${VOS_PACKAGE}
