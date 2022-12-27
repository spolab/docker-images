FROM alpine:latest

LABEL org.opencontainers.image.source=https://github.com/spolab/docker-images
LABEL org.opencontainers.image.description="Golang Runtime Image"
LABEL org.opencontainers.image.licenses=MIT

ARG DIR_HOME=/app

RUN \
# Update the operating system image
    apk update && \
    apk upgrade && \
# Create the build user
    adduser -h ${DIR_HOME} -D app

USER build

WORKDIR ${DIR_HOME}
