FROM ubuntu
WORKDIR /server
EXPOSE 5000
RUN apt-get update && apt-get install -y curl 
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs
COPY . .
RUN npm install
ENV API_URL=http://localhost/api
CMD ["npm", "start"]
