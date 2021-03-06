In order to simplify the tedious process of image annotation, here I use mtcnn face detection algorithm to realize automatic face annotation in video. Generated txt files and image files can be directly used in Labelimg or used as yolov3 dataset. 
Therefore, I rewrote the main content of test.py.


The following is the original author's description.


# mtcnn-pytorch
pytorch implementation of  face detection algorithm  MTCNN

### Usage MTCNN

Just download the repository and then do this

```
from src.detector import detect_faces
from src.utils import show_bboxes
from PIL import Image

image = Image.open('images/test3.jpg')
bounding_boxes, landmarks = detect_faces(image)
image = show_bboxes(image, bounding_boxes, landmarks)
image.show()
```

### Requirements

- pytorch 0.4
- Pillow, numpy

### Credit

This implementation is heavily inspired by:

- [pangyupo/mxnet_mtcnn_face_detection](https://github.com/pangyupo/mxnet_mtcnn_face_detection)
- https://github.com/kpzhang93/MTCNN_face_detection_alignment
- https://github.com/TropComplique/mtcnn-pytorch

### Reference

**MTCNN:** [Joint Face Detection and Alignment using Multi-task Cascaded Convolutional Networks](https://arxiv.org/abs/1604.02878).

