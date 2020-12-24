FROM ubuntu:18.04

EXPOSE 25565

RUN apt-get update && apt-get upgrade -y && \
	apt-get install -y wget && \
	apt-get install -y openjdk-8-jre-headless screen

WORKDIR minecraft
RUN wget https://launcher.mojang.com/v1/objects/3737db93722a9e39eeada7c27e7aca28b144ffa7/server.jar -O minecraft_server.1.13.jar
RUN echo "eula=true" > eula.txt

ENTRYPOINT java -Xms1024M -Xmx1024M -jar minecraft_server.1.13.jar -o true
