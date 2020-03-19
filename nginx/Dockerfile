FROM nginx:stable
MAINTAINER Tom **@**.com
RUN /bin/cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime \
  && echo 'Asia/Shanghai' >/etc/timezone && touch /var/log/nginx/access80.log && /var/log/nginx/access443.log
