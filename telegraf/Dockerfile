FROM balenalib/raspberrypi3

RUN curl -o /tmp/telegraf.deb https://dl.influxdata.com/telegraf/releases/telegraf_1.11.0-1_armhf.deb
RUN dpkg -i /tmp/telegraf.deb && rm /tmp/telegraf.deb

COPY telegraf.conf /etc/telegraf/telegraf.conf
COPY entry.sh /entry.sh
RUN chmod +x /entry.sh

CMD /entry.sh
