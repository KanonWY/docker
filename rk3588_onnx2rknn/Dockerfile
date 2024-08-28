FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && \
    apt install -y --no-install-recommends python3 python-is-python3 python3-dev python3-pip&& \
    apt install -y --no-install-recommends gcc vim libprotobuf-dev zlib1g zlib1g-dev libsm6 && \
    apt install -y --no-install-recommends libgl1 libglib2.0-0 android-tools-adb

COPY ./rknn_toolkit2-1.6.0+81f21f4d-cp38-cp38-linux_x86_64.whl rknn_toolkit2-1.6.0+81f21f4d-cp38-cp38-linux_x86_64.whl

COPY ./requirements.txt requirements.txt

RUN pip3 install -r requirements.txt

RUN pip3 install rknn_toolkit2-1.6.0+81f21f4d-cp38-cp38-linux_x86_64.whl
