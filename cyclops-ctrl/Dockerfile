FROM golang:1.22.5-alpine as build

WORKDIR /build

COPY go.mod ./
RUN go mod download
RUN go mod tidy

COPY ./ ./

RUN mkdir /build/bin
RUN go build -o /build/bin ./...

FROM alpine:3.20.0

ARG VERSION
ENV CYCLOPS_VERSION=$VERSION

WORKDIR /app

RUN mkdir /app/bin

COPY --from=build /build/bin/main /app/bin/ctrl

CMD ["/app/bin/ctrl"]
