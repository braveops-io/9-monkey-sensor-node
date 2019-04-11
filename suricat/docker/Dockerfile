# Dockerfile to build a Suricata docker container

# Set the base image to Ubuntu
FROM ubuntu
MAINTAINER Mattias

# Update and install deps
RUN apt update &&  apt install -y software-properties-common wget apt-transport-https

# Add the Suricata repository
RUN add-apt-repository -y ppa:oisf/suricata-stable

# Update the repos and install Suricata
RUN apt update && apt install -y suricata

# Copy the suricata config to its config location
ADD suricata.yaml /etc/suricata/suricata.yaml

# Start the Suricata/Filebeat service when the container is started
CMD service suricata start && tail -F /var/log/suricata/suricata.log
