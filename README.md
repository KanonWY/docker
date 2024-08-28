## docker for model 3588

xxx.tar is amd64 version docker image!

## how to use
### pt to onnx
```bash
# run in ultralytics_yolov8
docker run -it -v ${PWD}:/root/ws rk3588_pt2onnx:latest bash

# in docker
cd /root/ws
export PYTHONPATH=./
python ./ultralytics/engine/exporter.py
```

### onnx to rknn
```bash
# run in rk3588-convert-to-rknn
docker run -it -v ${PWD}:/root/ws rk3588_onnx2rknn:latest bash
# in docker
python convert.py yolov8n.onnx rk3588 i8 yolov8n.rknn
```
