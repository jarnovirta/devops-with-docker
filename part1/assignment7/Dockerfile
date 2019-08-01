FROM ubuntu
RUN apt-get update && apt-get install curl -y
WORKDIR /curler
COPY ./curler.sh .
RUN chmod +x ./curler.sh
CMD ["./curler.sh"]
