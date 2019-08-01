FROM node:alpine as build-stage
WORKDIR /scr
COPY . .
RUN npm install && \
    npm run build

FROM node:alpine
WORKDIR /server
EXPOSE 5000
COPY --from=build-stage /scr/dist/ /server/dist
RUN npm install -g serve && \
      chown -R node /server
USER node
ENV API_URL=http://localhost:8000
CMD ["serve", "-s", "-l", "5000", "dist"]
