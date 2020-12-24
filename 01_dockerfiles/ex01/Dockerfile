FROM debian:latest

#update and intstall wget
RUN apt-get update
RUN apt-get install wget -y
RUN apt-get install tar -y
RUN apt-get install bzip2 -y

ENV TS3SERVER_LICENSE=accept

RUN wget http://dl.4players.de/ts/releases/3.0.13.4/teamspeak3-server_linux_amd64-3.0.13.4.tar.bz2
RUN tar -xvf teamspeak3-server_linux_amd64-3.0.13.4.tar.bz2
WORKDIR teamspeak3-server_linux_amd64
EXPOSE 30033 10011 9987

ENTRYPOINT sh ts3server_minimal_runscript.sh
