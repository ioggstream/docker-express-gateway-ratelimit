FROM node:latest


RUN npm install -g sanyamdogra/express-gateway#update-rate-limit && \
    eg gateway create -n modi -d modi  -t basic

WORKDIR /modi

# workaround as "eg" still uses the old ratelimit
RUN npm install sanyamdogra/express-gateway#update-rate-limit
    

ADD gateway.config.yml /modi/config/gateway.config.yml

ENTRYPOINT ["npm","start"]

