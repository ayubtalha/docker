# Specify a base image
FROM node:22-alpine

# Install some depenendencies
WORKDIR /usr/app
COPY ./package.json ./
RUN npm install
COPY ./ ./

# Default command
CMD ["npm","start"]