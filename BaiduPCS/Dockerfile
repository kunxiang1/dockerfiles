FROM lsiobase/alpine.arm64
ENV TZ=Asia/Shanghai VERSION 3.5.8
RUN apk update && apk upgrade\
	apk --no-cache add  no-cache bash  bash-doc  bash-completion wget unzip \
    && rm -rf /var/cache/apk/*  \
    && wget http://qiniu.zoranjojo.top/BaiduPCS-Go-${VERSION}-linux-arm64.zip \
      && unzip BaiduPCS-Go-${VERSION}-linux-arm64.zip \
      && mv BaiduPCS-Go-${VERSION}-linux-amd64/BaiduPCS-Go BaiduPCS-Go \
	  && rm -rf BaiduPCS-Go-${VERSION}-linux-arm64*\	  
      && chmod a+x BaiduPCS-Go \	  
VOLUME /Downloads
EXPOSE 5299
ENTRYPOINT ["./BaiduPCS-Go"]