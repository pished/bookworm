FROM golang:alpine
WORKDIR /bookworm

RUN apk update && apk add --no-cache gcc musl-dev git bash

COPY . .

RUN go build -ldflags '-w -s' -a -o ./bin/bookworm ./cmd/bookworm

CMD ["/bookworm/bin/bookworm"]
EXPOSE 8080