FROM ubuntu:18.10

#Ingrediten:
#	jdk-8u162-linux-x64.tar.gz

RUN buildDeps='gcc libc6 make ssh net-tools iputils-ping git curl telnet vim' \
	&& apt-get update	\
	&& apt-get install -y $buildDeps	\
	&& mkdir -p /opt/java/

COPY ./jdk-8u162-linux-x64.tar.gz  /opt/java/

RUN cd /opt/java/	\
	&& tar -zxvf jdk-8u162-linux-x64.tar.gz

ENV JAVA_HOME=/opt/java/jdk1.8.0_162
ENV PATH=$JAVA_HOME/bin:$PATH
ENV CLASSPATH=.:$JAVA_HOME/bin/dt.jar:$JAVA_HOME/lib/tools.jar 
