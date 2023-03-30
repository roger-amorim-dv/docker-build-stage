FROM golang as builder

WORKDIR /app
COPY bin/main /app/
ENTRYPOINT ./main

FROM alpine
WORKDIR /anotherpath
COPY --from=builder /app/main/ /anotherpath/
ENTRYPOINT ./main
