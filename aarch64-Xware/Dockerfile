FROM forumi0721/alpine-aarch64-base


RUN     apt-get update \
	&& apt-get install libc6:armhf zlib1g:armhf \
	&& ln -s /lib/ld-linux-armhf.so.3 /lib/ld-linux.so.3\

WORKDIR /xware
ADD Xware1.0.31_armel_v5te_glibc.tar.gz /xware
ADD monitor.sh /xware

VOLUME /data

ENTRYPOINT ["./monitor.sh"]
