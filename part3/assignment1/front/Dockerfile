FROM ubuntu
WORKDIR /server
EXPOSE 5000
COPY . .
RUN apt-get update && apt-get install -y curl && \
   curl -sL https://deb.nodesource.com/setup_10.x | bash && \
   apt install -y nodejs && \
   npm install && \
   apt-get purge -y --auto-remove curl && \
   rm -rf /var/lib/apt/lists/*   
ENV API_URL=http://localhost:8000
CMD ["npm", "start"]
