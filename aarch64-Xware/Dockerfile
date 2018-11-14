FROM forumi0721/alpine-armhf-base


RUN apk update && apk upgrade \
    && apk --no-cache add libc6 zlib1g\

WORKDIR /xware
ADD Xware1.0.31_armel_v5te_glibc.tar.gz /xware
ADD monitor.sh /xware

VOLUME /data

ENTRYPOINT ["./monitor.sh"]
