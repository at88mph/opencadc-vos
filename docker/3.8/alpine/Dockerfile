FROM python:3.8-alpine

RUN apk --no-cache add gcc git libffi-dev libxml2-dev libxslt-dev musl-dev openssl-dev
  
RUN pip install --no-cache-dir "git+git://github.com/opencadc/vostools.git@newstorage#egg=vos&subdirectory=vos"
