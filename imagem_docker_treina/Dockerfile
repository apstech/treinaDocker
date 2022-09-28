FROM debian:11

COPY entrypoint.sh /sbin/entrypoint.sh

RUN	\
  apt-get update \
  && apt-get install -y apache2 \
  && chmod 755 /sbin/entrypoint.sh \
  && service apache2 start

EXPOSE 80 443

# By default, simply start apache.
CMD ["/sbin/entrypoint.sh"]