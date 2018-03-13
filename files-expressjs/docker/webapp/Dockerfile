FROM node:9

ENV WORKDIR=/usr/src/app

# Create app directory
WORKDIR $WORKDIR

# build data
RUN date > /builddate
COPY ./node_modules $WORKDIR/node_modules
COPY ./bin $WORKDIR/bin
COPY ./public $WORKDIR/public
COPY ./routes $WORKDIR/routes
COPY ./views $WORKDIR/views

COPY ./app.js $WORKDIR/
COPY package*.json $WORKDIR/

EXPOSE 80
CMD [ "npm", "start" ]