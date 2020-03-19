FROM zookeeper:3.4.10

ENV ZOO_AUTOPURGE_SNAPRETAINCOUNT=10 ZOO_AUTOPURGE_PURGEINTERVAL=5 ZOO_MAX_CLIENT_CNXNS=10000
## according office image, add auto clean envirment to /conf/zoo.cfg....attention:olny office in first time create,please read for detail in /docker-entrypoint.sh
RUN sed -ri '/ZOO_MAX_CLIENT_CNXNS/aecho "autoPurge.purgeInterval=$ZOO_AUTOPURGE_PURGEINTERVAL" >> "$CONFIG"\necho "autoPurge.snapRetainCount=$ZOO_AUTOPURGE_SNAPRETAINCOUNT" >> "$CONFIG"' /docker-entrypoint.sh