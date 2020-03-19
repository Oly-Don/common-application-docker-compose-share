FROM jenkins:2.60.3

RUN  apt-get update && \
  apt-get install -y  git maven ant jdk8 && \
  ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
        rm -rf /var/lib/apt/lists/*    &&\
  chown -R jenkins:root /usr/share/ant  &&\
  chown -R jenkins:root /usr/share/maven
ENV M2_HOME=/usr/share/maven  ANT_HOME=/usr/share/ant JAVA_OPTS=-Dorg.apache.commons.jelly.tags.fmt.timeZone=Asia/Shanghai LANG=zh_CN.UTF-8 JENKINS_OPTS="--prefix=/jenkins/ $JENKINS_OPTS -Dfile.encoding=UTF-8" PATH=\$ANT_HOME\\bin:\$M2_HOME\\bin:$PATH

USER root

#ADD settings.xml /usr/share/maven/conf/settings.xml