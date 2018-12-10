# Pull base image.
FROM ubuntu:latest


# Install.
RUN \
apt-get update && \
apt-get -y upgrade && \
apt-get install -y build-essential && \
apt-get install --yes g++ && \
apt-get install --yes gcovr && \
apt-get install --yes ggcov && \
apt-get install --yes binutils && \
apt-get install --yes valgrind && \
apt-get install --yes python3


# Set environment variables.
ENV HOME /root

# Define working directory.
WORKDIR /root


# Define default command.
CMD ["bash"]

USER $NB_UID
