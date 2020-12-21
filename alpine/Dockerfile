FROM alpine:3.12.2

RUN sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories

RUN set -eux; \
    apk update && apk add --no-cache\ 
    curl \
    wget \
    tcpdump \
    make \
    tzdata \
    ;\
    cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime; \
    echo 'Asia/Shanghai' > /etc/timezone; \
    rm -rf /var/cache/apk/*;

WORKDIR /
CMD ["/bin/sh"]