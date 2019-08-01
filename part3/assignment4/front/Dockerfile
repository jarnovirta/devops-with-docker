FROM node:alpine
WORKDIR /server
EXPOSE 5000
COPY . .
RUN npm install && \
    chown -R node /server
USER node
ENV API_URL=http://localhost:8000
CMD ["npm", "start"]
