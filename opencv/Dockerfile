FROM hplustime/alpine-emscripten:wasm-latest
COPY ./wrapper.sh .
RUN git clone https://github.com/opencv/opencv.git --depth=1
RUN mkdir -p opencv/build && cd opencv/build && ../../wrapper.sh && make -j$(($(nproc)-1>0?$(nproc)-1:1))
RUN cp -r opencv/include/opencv* /usr/share/emscripten/system/include
RUN cp -r opencv/modules/*/include/opencv2/* /usr/share/emscripten/system/include/opencv2
