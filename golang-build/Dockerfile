FROM alpine:latest

ARG DIR_HOME=/build

RUN \
# Update the operating system image
    apk update && \
    apk upgrade && \
# Add the required tools
    apk add --no-cache go make protobuf && \
# Create the build user
    adduser -h ${DIR_HOME} -D build

USER build

RUN go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28 && \
    go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1

WORKDIR ${DIR_HOME}
