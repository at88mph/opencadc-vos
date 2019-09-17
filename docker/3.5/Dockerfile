FROM python:3.5-alpine

RUN apk --no-cache add gcc libxml2-dev musl-dev libxslt-dev \
  && pip install --no-cache-dir vos --upgrade --prefix /usr/local
