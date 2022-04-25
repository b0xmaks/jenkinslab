FROM openjdk:8u151-stretch

# Install packages 
RUN apt-get update && apt-get -y install apt-transport-https ca-certificates curl gnupg lsb-release software-properties-common maven

# Install docker
RUN curl -fsSL https://download.docker.com/linux/debian/gpg | gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
RUN add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/debian stretch stable"
RUN apt-get update
RUN apt-get -y install docker-ce docker-ce-cli containerd.io

# Clear cache
RUN apt-get clean