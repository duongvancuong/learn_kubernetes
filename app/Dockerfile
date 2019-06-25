# The official image of the node
FROM node:10-alpine
# ARG Version to define app version
ARG VERSION=1.0.0
# Create app directory inside image
WORKDIR /usr/src/app
# Set required environment variables
ENV NODE_ENV production
# Install app dependencies by copying package.json to image
COPY package.json .
# For npm@5 or later, copy package-lock.json as well
# COPY package.json package-lock.json ./
RUN npm install
# Bundle app source
COPY . .
# It will start the app on 3000 port of the container
EXPOSE 3000
CMD [ "npm", "start" ]
