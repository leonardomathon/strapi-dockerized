FROM strapi/base

# Let WatchTower know to ignore this container for checking
LABEL com.centurylinklabs.watchtower.enable="false"

WORKDIR /strapi

COPY ./package*.json ./

RUN npm install npm@latest -g

RUN npm install

COPY . .

ENV NODE_ENV production

RUN npm run build

EXPOSE 1337

CMD ["npm", "start"]