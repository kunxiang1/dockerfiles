FROM forumi0721/alpine-aarch64-base

WORKDIR /xware
ADD Xware1.0.31_armel_v5te_glibc.tar.gz .
ADD monitor.sh .
RUN cd / && apk update && apk upgrade \
    && apk --no-cache add libc6 zlib1g \
    && chmod a+x /xware/*\

VOLUME /data

ENTRYPOINT ["monitor.sh"]
