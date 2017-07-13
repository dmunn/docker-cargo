FROM centos:6
MAINTAINER David Munn

COPY files/rpms/mongo/2.4 /tmp/
RUN \
  rpm -ivh /tmp/mongo-10gen-2.4.13-mongodb_1.x86_64.rpm && \
  rpm -ivh /tmp/mongo-10gen-server-2.4.13-mongodb_1.x86_64.rpm && \
  rm -f /tmp/mongo-10gen-* 

VOLUME ["/data/db"]

WORKDIR /data

CMD ["mongod"]

EXPOSE 27017
EXPOSE 28017

