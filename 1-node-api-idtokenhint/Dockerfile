FROM mcr.microsoft.com/appsvc/node:12-lts

WORKDIR /usr/src/app

COPY package*.json ./

RUN npm install

COPY . .

ENV HOST 0.0.0.0
ENV PORT 8080
EXPOSE 8080

#CMD node app.js $CONFIGFILE $ISSUANCEFILE $PRESENTATIONFILE
RUN chmod +x docker-run.sh

ENTRYPOINT ["./docker-run.sh"]