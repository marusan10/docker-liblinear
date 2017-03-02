FROM alpine

ENV VERSION 2.11-1

RUN apk add --update --no-cache --virtual=.liblinear-deps \
        libgcc \
        libstdc++ \
        libgomp \
        libatomic \
    && apk add --update --no-cache --virtual=.liblinear-dev-deps \
        make \
        g++ \
        gcc \
        wget \
        unzip \
    && mkdir -p /usr/local/src \
    && cd /usr/local/src \
    && wget --no-check-certificate https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/multicore-liblinear/liblinear-multicore-${VERSION}.zip \
    && unzip liblinear-multicore-${VERSION}.zip \
    && cd liblinear-multicore-${VERSION} \
    && make all \
    && ln -s /usr/local/src/liblinear-multicore-${VERSION}/train /usr/local/bin/train \
    && ln -s /usr/local/src/liblinear-multicore-${VERSION}/predict /usr/local/bin/predict \
    && apk del .liblinear-dev-deps

WORKDIR /data

VOLUME /data

