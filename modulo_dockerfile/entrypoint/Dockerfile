FROM alpine

RUN apk add --no-cache git nano npm

# não permite sobrescrever comandos
ENTRYPOINT [ "ping" ]
CMD [ "localhost" ]