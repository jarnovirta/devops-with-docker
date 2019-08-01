FROM node:alpine as build-stage
WORKDIR /src
COPY . .
RUN npm install && \
    npm run build

FROM node:alpine
WORKDIR /app
EXPOSE 3000
COPY --from=build-stage /src/build/ /app/build
RUN npm install -g serve && \
      chown -R node /app
USER node
CMD ["serve", "-s", "-l", "3000", "build"]
