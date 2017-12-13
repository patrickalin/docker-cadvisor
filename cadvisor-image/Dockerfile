FROM google/cadvisor:v0.28.3
COPY .htpasswd /.htpasswd
COPY localtime /etc/localtime
RUN apk add --update bash curl
#HEALTHCHECK --interval=10s --timeout=10s --retries=3 CMD curl -f http://localhost:8080/ || exit 1
#ENTRYPOINT ["/usr/bin/cadvisor", "--http_auth_file", ".htpasswd", "-logtostderr"]
ENTRYPOINT ["/usr/bin/cadvisor", "-logtostderr"]
