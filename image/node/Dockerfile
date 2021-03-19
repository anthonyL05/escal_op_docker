FROM node:10.19.0


RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

USER node
RUN mkdir /home/node/.npm-global
ENV PATH=/home/node/.npm-global/bin:$PATH
ENV NPM_CONFIG_PREFIX=/home/node/.npm-global
RUN npm install -g @angular/cli
RUN npm i npm@latest -g

EXPOSE 4200

CMD ["npm", "start"]