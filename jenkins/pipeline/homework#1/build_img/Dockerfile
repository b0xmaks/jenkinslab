FROM openjdk:8u151-stretch

# Install packages 
RUN apt-get update && apt-get -y install apt-transport-https ca-certificates curl gnupg lsb-release software-properties-common maven docker-ce docker-ce-cli containerd.io

# Clear cache
RUN apt-get clean