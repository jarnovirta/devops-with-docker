FROM node:alpine
WORKDIR /backend
EXPOSE 8000
COPY . .
RUN npm install && \
    chown -R node /backend
USER node
ENV FRONT_URL=http://localhost:5000
CMD ["npm", "start"]
