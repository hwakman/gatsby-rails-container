FROM node:12.18.4

RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

COPY package.json ./
COPY yarn.lock ./

RUN yarn global add gatsby-cli
RUN gatsby telemetry --disable
RUN yarn install

CMD [ "gatsby", "develop", "--host=0.0.0.0" ]
