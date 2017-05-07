FROM hplustime/emscripten-wasm
COPY ./wrapper.sh .
RUN git clone https://github.com/opencv/opencv.git --depth=1
RUN mkdir -p opencv/build && cd opencv/build && ../../wrapper.sh && make -j$(($(nproc)-1>0?$(nproc)-1:1))
