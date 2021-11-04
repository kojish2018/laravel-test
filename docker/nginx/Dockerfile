FROM nginx:latest

RUN apt-get update && apt-get install -y \
    openssl \
    ssl-cert \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

ADD config/ssl.conf /etc/nginx/ssl/ssl.conf
ADD config/entrypoint.sh /opt/entrypoint.sh

RUN chmod a+x /opt/entrypoint.sh
# RUN /bin/bash -c "source /opt/entrypoint.sh /etc/nginx/ssl local-asas-back.com"
RUN /bin/bash -c "source /opt/entrypoint.sh /etc/nginx/ssl local-test-back.com"
