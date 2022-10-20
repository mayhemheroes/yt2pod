FROM golang:1.18 as builder

ADD . /yt2pod
WORKDIR /yt2pod
RUN go mod tidy
RUN go build

# Package Stage
FROM debian:bookworm-slim
COPY --from=builder /yt2pod/yt2pod /
