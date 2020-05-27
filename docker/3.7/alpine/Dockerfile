FROM python:3.7-alpine

RUN apk --no-cache add gcc libffi-dev libxml2-dev libxslt-dev musl-dev openssl-dev \
  && pip install --no-cache-dir git+git://github.com/opencadc/vostools.git@newstorage#egg=vos&subdirectory=vos --upgrade --prefix /usr/local
