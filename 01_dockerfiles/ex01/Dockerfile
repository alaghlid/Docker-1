FROM debian
ENV TS3SERVER_LICENSE=accept
RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get install wget bzip2 -y
RUN wget http://dl.4players.de/ts/releases/3.8.0/teamspeak3-server_linux_amd64-3.8.0.tar.bz2
RUN tar -xvsf teamspeak3-server_linux_amd64-3.8.0.tar.bz2
RUN rm -f teamspeak3-server_linux_amd64-3.8.0.tar.bz2
EXPOSE 9987/udp 10011/tcp 30033/tcp
WORKDIR teamspeak3-server_linux_amd64
ENTRYPOINT sh ts3server_minimal_runscript.sh start

# docker build -f Dockerfile -t team .
# docker run -it -p 9987:9987/udp -p 10011:10011/tcp -p 30033:30033/tcp  team 
