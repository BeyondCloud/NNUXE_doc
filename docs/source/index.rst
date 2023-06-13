NNUXE
===================================

Neural Network Universal format Xchanger(NNUXE) is a multifunctional, neural
network processing software which helps users convert their model format to
to another. The product supports a wide range of model formats, including:

- Tensorflow `*.pb`, `*.h5`, `SavedModel`, `*.tflite`, `mlir` and `*.ckpt`
- Pytorch `*.pt`, `TorchScript`
- ONNX `*.onnx`
- Caffe `*.caffemodel/ *.prototxt`
- Openvino `*.xml/ *.bin`
- TVM `relayir`
- Tensorrt

Each model format listed above are presented in one of the node of the graph
called `Default Converter Graph`. For each starting node and ending node
selected by the user, our algorithm find all possible paths between them and try
all the path to convert the model until the end node is reached. Besides model
format conversion, we provide optimization options for `*.onnx` model, such as
shape inference, constant folding, etc.


Dependencies
===================================

Our tool depends on several third party libraies, including:

- `tf2onnx`
  - https://github.com/onnx/tensorflow-onnx
- `onnxruntime`
  - https://onnxruntime.ai/docs/get-started/with-python.html
- `tvm.relay`
  - https://tvm.apache.org/docs/reference/api/python/relay/index.html
- `Openvino Model Optimizer`
  - https://docs.openvino.ai/2022.3/openvino_docs_MO_DG_Deep_Learning_Model_Optimizer_DevGuide.html
- `openvino2tensorflow`
  - https://pypi.org/project/openvino2tensorflow/
- `ONNX Simplifier`
  - https://github.com/daquexian/onnx-simplifier
- `ONNX version_converter`
- `tf-mlir-translate`


Contents
--------
.. toctree::
   usage
   api
