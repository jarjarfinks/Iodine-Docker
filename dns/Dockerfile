FROM ubuntu:latest
RUN apt-get update -y
RUN apt-get install -y iodine
ENTRYPOINT ["iodined"]
CMD ["-f" , "-P", ${PASSWORD}, ${IP}, ${DNS}]
