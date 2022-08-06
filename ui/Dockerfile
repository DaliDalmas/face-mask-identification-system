FROM node:lts-alpine

# install simple http server for the static content
RUN npm install -g http-server

# make the app folder the curent working directory
WORKDIR /app

# copy both package.json and package-lock.json if available
COPY fmis-ui/package*.json .

# install project dependencies
RUN npm install

# copy the project files from the current directory to the app directory
COPY fmis-ui .

# build app for production with minification
RUN npm run build

EXPOSE 8080
CMD ["http-server", "dist"]