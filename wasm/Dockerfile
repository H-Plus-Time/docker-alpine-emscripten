FROM mhart/alpine-node:latest
RUN ln -s /usr/share/emscripten ../emsdk-portable && \
    echo http://dl-cdn.alpinelinux.org/alpine/edge/testing >> /etc/apk/repositories && \
    echo http://dl-cdn.alpinelinux.org/alpine/edge/community >> /etc/apk/repositories
RUN apk --update add yarn emscripten emscripten-libs-asmjs make cmake emscripten-libs-wasm binaryen git
