FROM maven:3.8.5-openjdk-8
# Install packages
RUN apt update && apt upgrade -y
# Install docker 18.03
RUN apt -y install apt-transport-https ca-certificates curl
RUN curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
RUN add-apt-repository 'https://download.docker.com/linux/ubuntu \ $(lsb_release -cs) stable"'
RUN apt update
RUN apt -y install docker-ce docker-ce-cli containerd.io
# Clear cache
RUN apt clean