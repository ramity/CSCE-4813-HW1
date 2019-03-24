FROM gcc:4.8.4

# docker config/meta
MAINTAINER github.com/ramity
WORKDIR /var/cpp

# download deps
RUN apt-get update -y
RUN apt-get install -y mesa-common-dev
RUN apt-get install -y freeglut3-dev

# download source
RUN wget -O /var/cpp/src.tar http://www.csce.uark.edu/~jgauch/4813/src/src.tar
RUN tar -xvf /var/cpp/src.tar
# RUN cd /var/cpp/src/jpg && make clean && make
# RUN cd /var/cpp/src/libim && make clean && make
RUN cd /var/cpp/src && make

# docker execution
ENTRYPOINT ["tail","-f","/dev/null"]
