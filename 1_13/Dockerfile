FROM golang:1.16

WORKDIR /app

COPY . . 
EXPOSE 8080
RUN go build .
RUN go test ./...

CMD ["./server"]
