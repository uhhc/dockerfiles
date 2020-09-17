FROM golang:1.13-alpine3.10

# Install needed software
RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.tuna.tsinghua.edu.cn/g' /etc/apk/repositories
RUN apk add --no-cache git make cmake build-base pkgconfig; \
    # Build goose
    export GOPROXY=https://goproxy.cn; \
    go get -v -tags nosqlite3 github.com/steinbacher/goose/cmd/goose
