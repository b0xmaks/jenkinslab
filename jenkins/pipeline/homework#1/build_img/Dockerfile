FROM openjdk:8u151-stretch

# Install pacakges
RUN apt-get update

# Install maven 3.8.5
RUN apt-get -y install ca-certificates curl software-properties-common
RUN mkdir -p /usr/local/apache-maven/apache-maven-3.8.5 && \
    wget https://dlcdn.apache.org/maven/maven-3/3.8.5/binaries/apache-maven-3.8.5-bin.tar.gz --no-check-certificate && \
    tar -xvf apache-maven-3.8.5-bin.tar.gz -C /usr/local/apache-maven/apache-maven-3.8.5 && \
    rm apache-maven-3.8.5-bin.tar.gz
ENV PATH=$PATH:/opt/apache-maven-3.8.5/bin

# Install docker 18.03
RUN curl -fsSL https://download.docker.com/linux/debian/gpg | apt-key add -
RUN add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian stretch stable"
RUN apt-get update
RUN apt-get -y install docker-ce=18.03.1~ce-0~debian

# Clear cache
RUN apt-get clean