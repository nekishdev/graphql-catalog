FROM golang:1.14.2

MAINTAINER nekishdev

ENV PROJECT_DIR=/app
ENV GOPROXY=direct

RUN mkdir -p $PROJECT_DIR

WORKDIR $PROJECT_DIR

COPY . .

RUN go mod vendor

RUN go build -o ./server

EXPOSE 80 443

CMD ["./server"]