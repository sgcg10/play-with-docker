FROM komljen/ubuntu
LABEL Salvador Cruz

ENV USER root
ENV PASS hidethisalwaysplease

RUN \
  apt-get update && \
  apt-get -y install \
          mysql-server-5.5 && \
  rm -rf /var/lib/apt/lists/*

COPY my.cnf /etc/mysql/my.cnf
COPY start.sh start.sh

VOLUME ["/var/lib/mysql"]

RUN rm /usr/sbin/policy-rc.d
CMD ["/start.sh"]

EXPOSE 3306