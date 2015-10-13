# Lightweight Docker image for the AWS CLI based on Alpine Linux and 
# the Dockerfile of https://registry.hub.docker.com/u/anigeo/awscli/

FROM alpine:latest

MAINTAINER Manuel M T Chakravarty <chak@justtesting.org>

RUN \
  mkdir -p /aws && \
  apk -Uuv add groff less python py-pip && \
  pip install awscli && \
  apk --purge -v del py-pip && \
  rm -r /var/cache/apk/* /root/.cache

WORKDIR /aws
ENTRYPOINT ["sh", "-c"]
