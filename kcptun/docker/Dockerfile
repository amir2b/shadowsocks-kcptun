FROM alpine
LABEL maintainer="Amir Bashiri"

ENV KCPTUN_VERSION 20200701
ENV KCPTUN_FILE kcptun-linux-amd64-${KCPTUN_VERSION}.tar.gz
ENV KCPTUN_URL https://github.com/xtaci/kcptun/releases/download/v${KCPTUN_VERSION}/${KCPTUN_FILE}

RUN set -xe \
    && echo -e "http://nl.alpinelinux.org/alpine/v3.5/main\nhttp://nl.alpinelinux.org/alpine/v3.5/community" > /etc/apk/repositories \
    && apk add --no-cache curl \
    && curl -sSL ${KCPTUN_URL} | tar xz -C /usr/local/bin \
    && apk del curl

ENTRYPOINT ["server_linux_amd64", "--target", "shadowsocks:8388"]
ENV MODE=fast3
ENV SOCKBUF=16777217
ENV DSCP=46
ENV AUTOEXPIRE=900
CMD ["--mode", "${MODE}", "--sockbuf", ${SOCKBUF}, "--dscp", ${DSCP}, "--autoexpire", ${AUTOEXPIRE}, "--nocomp"]