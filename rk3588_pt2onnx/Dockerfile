# Version 1.0
FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

# RUN sed -i "s/archive.ubuntu.com/mirrors.cloud.tencent.com/g" /etc/apt/sources.list && \
#     sed -i "s/security.ubuntu.com/mirrors.cloud.tencent.com/g" /etc/apt/sources.list && \
#     sed -i "s/ports.ubuntu.com/mirrors.cloud.tencent.com/g" /etc/apt/sources.list && \
COPY ./requirements.txt /tmp/requirements.txt
RUN	apt update && \
	apt install -y --no-install-recommends python3 python3-pip && \
  pip install -i https://pypi.tuna.tsinghua.edu.cn/simple -r /tmp/requirements.txt

RUN apt install -y --no-install-recommends libgl-dev libglib2.0-0 python-is-python3 && \
    pip install -i https://pypi.tuna.tsinghua.edu.cn/simple  onnx

