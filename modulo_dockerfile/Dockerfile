FROM alpine

#LABEL chave e valor
LABEL MAINTAINER="Rafael Martins <<rafaelmartins@025@outlook.com>>"
LABEL APP_VERSION="1.0.0"

#ENV chave e valor
ENV NPM_VERSION=8 ENVIRONMENT=PROD

RUN apk add --no-cache git nano npm

WORKDIR /usr/share/myapp

RUN npm build

#copy é mais limitado
#somente copiar arquivos para dentro do container
COPY copy.txt copy.txt

#add tem mais recursos
#copiar tar.gz e desconpactar para dentro do destino
#ou passar arquivo por url
ADD add.tar.gz ./
ADD https://api.github.com/users/ohrafaelmartins ohrafaelmartins.json

RUN adduser --disabled-password rafael

USER rafael

EXPOSE 9090