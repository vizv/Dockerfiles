# NOTE: use -v to mount data volume to /data/db
#     and config volume (read-only) to /config:ro

FROM centos
MAINTAINER Viz <viz@linux.com>

# add mongo db repo
ADD mongodb.repo /etc/yum.repos.d/mongodb.repo

RUN yum install -y mongodb-org-server

ENTRYPOINT ["/usr/bin/mongod"]

CMD ["--config", "/config/mongodb.conf"]
