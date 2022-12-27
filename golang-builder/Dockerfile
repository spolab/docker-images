FROM alpine:latest

LABEL org.opencontainers.image.source=https://github.com/spolab/docker-images
LABEL org.opencontainers.image.description="Golang Build Toolbox"
LABEL org.opencontainers.image.licenses=MIT

ARG DIR_HOME=/build

ENV GOPATH=/usr/local/share/go

RUN mkdir -p ${GOPATH} && \
# Update the operating system image
    apk update && \
    apk upgrade && \
# Add the required tools
    apk add --no-cache go make protobuf docker-cli

RUN go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28 && \
    go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1 && \
    ln -s ${GOPATH}/bin/* /usr/local/bin

WORKDIR ${DIR_HOME}
