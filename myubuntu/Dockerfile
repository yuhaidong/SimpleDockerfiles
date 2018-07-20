FROM ubuntu:18.10

RUN buildDeps='gcc libc6 make ssh net-tools iputils-ping git curl telnet' \
	&& apt-get update \
	&& apt-get install -y $buildDeps
