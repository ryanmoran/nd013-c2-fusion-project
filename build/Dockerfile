# docker run -it \
#   -v $PWD:/workspace \
#   -v /tmp/.X11-unix:/tmp/.X11-unix \
#   -e DISPLAY=$DISPLAY \
#   -e QT_X11_NO_MITSHM=1 \
#   --network host \
#   --gpus all \
#   sensor-fusion:project

FROM ubuntu:focal
ENV LANG C.UTF-8

RUN apt-get -qqy update \
  && DEBIAN_FRONTEND=noninteractive apt-get -qqy --no-install-recommends install \
    ffmpeg \
    libegl1 \
    libgl1 \
    libglvnd0 \
    libglx0 \
    libgtk-3-dev \
    libx11-6 \
    libxext6 \
    software-properties-common \
  && rm -rf /var/lib/apt/lists/*

RUN apt-get -qqy update && \
    add-apt-repository ppa:deadsnakes/ppa -y && \
    apt-get -qqy install python3.7 python3-pip
RUN ln -s $(which python3) /usr/local/bin/python

COPY requirements.txt .
RUN python -m pip install --upgrade pip
RUN python -m pip install -r requirements.txt

ENV GDK_SYNCHRONIZE true
ENV NVIDIA_VISIBLE_DEVICES all
ENV NVIDIA_DRIVER_CAPABILITIES graphics,utility,compute

WORKDIR /workspace
ENTRYPOINT [ "bash" ]
