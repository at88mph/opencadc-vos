ARG OPENCADC_PYTHON_VERSION=3.11

FROM python:${OPENCADC_PYTHON_VERSION}-slim as builder

ARG VOS_PACKAGE=vos

RUN apt-get update \
    && apt-get install -y gcc git libc-dev libffi-dev libmagic-dev libssl-dev libxslt-dev make

RUN pip install --no-cache-dir ${VOS_PACKAGE}


FROM python:${OPENCADC_PYTHON_VERSION}-slim

ARG OPENCADC_PYTHON_VERSION

# this is for sure required
COPY --from=builder /usr/local/lib/python${OPENCADC_PYTHON_VERSION}/site-packages /usr/local/lib/python${OPENCADC_PYTHON_VERSION}/site-packages

# this depends on what you are installing
COPY --from=builder /usr/local/bin /usr/local/bin
