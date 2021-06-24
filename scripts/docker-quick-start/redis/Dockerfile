FROM redis:latest

MAINTAINER Tommy Elmesewdy <r1tommy@gmail.com>
RUN echo "changed"
#RUN chmod o+r /etc/resolv.conf
#RUN echo "91.189.92.201 archive.ubuntu.com" >> /etc/hosts
RUN apt-get update
RUN apt-get install -y gettext-base

COPY redis.conf /etc/redis/redis.conf.template
COPY start.sh /start.sh

ENTRYPOINT [ "/bin/bash", "/start.sh" ]
