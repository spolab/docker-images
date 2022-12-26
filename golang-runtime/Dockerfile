FROM alpine:latest

ARG DIR_HOME=/app

RUN \
# Update the operating system image
    apk update && \
    apk upgrade && \
# Create the build user
    adduser -h ${DIR_HOME} -D app

USER build

WORKDIR ${DIR_HOME}
