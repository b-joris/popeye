FROM node:10
COPY . /result
WORKDIR /result
RUN npm install
EXPOSE 80
CMD [ "node", "server.js" ]