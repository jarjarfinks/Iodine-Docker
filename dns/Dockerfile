FROM ubuntu:latest
RUN apt-get update -y
RUN apt-get install -y iodine
COPY ./start.sh /start.sh
RUN chmod +x /start.sh
ENTRYPOINT ["sh"]
CMD [ "/start.sh"]
