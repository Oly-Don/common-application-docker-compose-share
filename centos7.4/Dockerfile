FROM centos:centos7.4.1708

user root
RUN /bin/cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime  && \
    useradd appuser  && \
    echo u6hCwUvd0w7uwjloHEPgVhwej65HTw | passwd --stdin appuser  && \
    echo 'Asia/Shanghai' >/etc/timezone && \
    yum -y update
ENV TZ=Asia/Shanghai