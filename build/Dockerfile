# docker run -it \
#   -v $PWD:/workspace \
#   -v /tmp/.X11-unix:/tmp/.X11-unix \
#   -e DISPLAY=$DISPLAY \
#   --network host \
#   sensor-fusion:project

FROM ubuntu:focal
ENV LANG C.UTF-8

RUN apt-get -qqy update \
  && DEBIAN_FRONTEND=noninteractive apt-get -qqy --no-install-recommends install \
    software-properties-common \
    libgtk-3-dev

RUN apt-get -qqy update && \
    add-apt-repository ppa:deadsnakes/ppa -y && \
    apt-get -qqy install python3.7 python3-pip
RUN ln -s $(which python3) /usr/local/bin/python

COPY requirements.txt .
RUN python -m pip install --upgrade pip
RUN python -m pip install -r requirements.txt

ENV GDK_SYNCHRONIZE true
WORKDIR /workspace
ENTRYPOINT [ "bash" ]
