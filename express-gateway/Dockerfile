FROM node:latest


RUN npm install -g express-gateway && \
    eg gateway create -n modi -d modi  -t basic 

ADD gateway.config.yml /modi/config/gateway.config.yml

WORKDIR /modi
ENTRYPOINT ["npm","start"]

