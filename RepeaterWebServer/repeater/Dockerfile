FROM ubuntu
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && yes | apt-get upgrade && yes | apt-get install git
RUN yes | apt-get install linux-headers-5.8.0-48-generic libx11-6 libx11-dev x-window-system-core x-window-system libxtst6 psmisc build-essential
EXPOSE 5500 5901

WORKDIR /progetto
RUN git clone https://github.com/DamianoP/uvncrep017-ws.git
WORKDIR /progetto/uvncrep017-ws/uvncRepeater
COPY ./uvncrepeater  /progetto/uvncrep017-ws/uvncRepeater/uvncrepeater 
RUN make 
RUN ["chmod", "u+x", "./install.sh"]
RUN make install
RUN ["chmod", "+x", "/etc/init.d/uvncrepeater"]

RUN useradd  -s /sbin/nologin uvncrep
COPY ./uvncrepeater.ini  /etc/uvnc/uvncrepeater.ini 
COPY ./entrypoint.sh /usr/bin/entrypoint.sh
ENTRYPOINT ["/usr/bin/entrypoint.sh"]
