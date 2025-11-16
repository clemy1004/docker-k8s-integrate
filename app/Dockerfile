FROM node:10-alpine
WORKDIR /app
COPY package.json ./
RUN yarn install --production
COPY app/ ./
CMD ["node", "src/index.js"]