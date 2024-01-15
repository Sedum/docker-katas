FROM golang:1.13.2 as builder
WORKDIR /src
ADD . /src/
RUN cd /src && go build -o goapp

FROM scratch
WORKDIR /app
COPY --from=builder /src/goapp /app/
CMD ["./goapp"]