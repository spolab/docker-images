FROM alpine:latest

LABEL org.opencontainers.image.source=https://github.com/spolab/docker-images
LABEL org.opencontainers.image.description="Golang Runtime Image"
LABEL org.opencontainers.image.licenses=MIT

ARG HOME=/runner
ARG BIN

RUN \
# Update the operating system image
    apk update && \
    apk upgrade && \
    apk add gcompat && \
# Create the build user
    adduser -h ${HOME} -D runner

USER runner

WORKDIR ${HOME}
