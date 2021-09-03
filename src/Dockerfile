FROM golang:latest
WORKDIR /goapp
ADD goapp.go .
RUN go build goapp.go

FROM alpine:latest
WORKDIR /goapp/
COPY --from=0 /goapp/goapp ./
CMD ["./goapp"]