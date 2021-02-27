FROM alpine

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