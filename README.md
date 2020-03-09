# lethanhquang tiny-yolov3-Android
YOLOv3 implementation with Tensorflow on Android

This project contains an example of YoloV3 implementation on Android, the YoloV3 model was implemented through the library 
``org.tensorflow:tensorflow-android``.

Below is a list of steps taken to convert the YoloV3 model from darkflow to tensorflow for Android (command launched on Ubuntu ):

  ```
  python3 main.py \
    --cfg 'data/yolov3-tiny.cfg' \
    --weights 'data/yolov3-tiny.weights' \
    --output 'data/' \
    --prefix 'yolov3-tiny/' \
    --gpu 0
  ```
 * launch freeze_graph to have a single bp graph file:
 ```
  freeze_graph  \
  --input_graph yolov3-tiny.pb  \
  --input_checkpoint yolov3-tiny.ckpt  \
  --input_binary=true  \
  --output_graph=ultimate_yolov3.bp  \
  --output_node_names=yolov3-tiny/convolutional10/BiasAdd
  ```

still update .....

For more detail about Yolo look at offical page https://pjreddie.com/darknet/yolo/
