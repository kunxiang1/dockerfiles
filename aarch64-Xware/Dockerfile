FROM forumi0721/alpine-aarch64-base


RUN cd / && apk update && apk upgrade \
    && apk --no-cache add libc6 zlib1g tar \
    && chmod a+x /xware/*\

WORKDIR /xware
ADD Xware1.0.31_armel_v5te_glibc.tar.gz /xware
ADD monitor.sh /xware

VOLUME /data

ENTRYPOINT ["monitor.sh"]
