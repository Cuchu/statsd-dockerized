FROM debian:8
run apt-get update && apt-get install -yq git nodejs npm

RUN npm install -g n

run apt-get install -yq wget
RUN n stable

RUN git clone https://github.com/Cuchu/nodejs-statsd-mysql-backend.git /opt/nodejs-statsd-mysql-backend

RUN cd /opt/smb ; npm install mysql
RUN cd /opt/smb ; npm install sequence

RUN git clone https://github.com/etsy/statsd /opt/statsd
RUN apt-get install -yq wget 

CMD node /opt/statsd/stats.js /opt/config/statsd.config.js
