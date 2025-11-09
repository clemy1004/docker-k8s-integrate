FROM node:10-alpine AS service
WORKDIR /app
COPY . .
RUN yarn install --production
CMD ["node", "app/src/index.js"]

FROM mysql:5.7 AS database
