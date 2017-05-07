FROM mhart/alpine-node:latest
RUN ln -s /usr/share/emscripten ../emsdk-portable && \
    echo http://dl-cdn.alpinelinux.org/alpine/edge/testing >> /etc/apk/repositories && \
    echo http://dl-cdn.alpinelinux.org/alpine/edge/community >> /etc/apk/repositories
RUN apk --no-cache add emscripten emscripten-libs-asmjs emscripten-libs-wasm
RUN apk --no-cache add binaryen closure-compiler make cmake git coreutils yarn
