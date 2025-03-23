# YOLO-object-detection-with-custom-dataset

In this we are detecting objects in a room using custom dataset

## YOLO Architecture :
1. Yolo model model process images in real time at 45 frames per second. In YOLO the image is divided into a grid. The processing of these grid cells occurs in parallel not sequentially.
2. This parallel processing is one of the key factors that makes YOLO so fast and efficient.
3. The input image is divided into S * S grids( 5 * 5, 7 * 7, 13 * 13 depending on YOLO version)
4. The entire image is passed through a single CNN in one forward pass.
5. For each grid cell, the network predicts : B bounding boxes and their confidence scores, C class probabilities.
6. The predictions are made for all grid cells concurrently not by one.
7. This network has 24 convolutional layers followed by two fully connected layers.
8. Final layer predicts both class probabilities and bounding box coordinates.
9. Linear activation function is used for final layer and all other layers use leaky rectified linear activation
10. Bounding box coordinates: Linear activation
    If any object is there or not: Sigmoid
    Class Prediction: Linear activation in the network and softmax applied in post processing
    In the network itself , linear activation is used for class scores
    During post processing , softmax is applied to the scores to get probabilities.

![](https://github.com/Srishti002/YOLO-object-detection-with-custom-dataset/blob/main/Screenshot%202025-03-23%20235753.png)
![](https://github.com/Srishti002/YOLO-object-detection-with-custom-dataset/blob/main/Screenshot%202025-03-23%20235835.png)

## Dataset:

https://universe.roboflow.com/yolo-ysajs/room-uzsl0/dataset/1

### YOLO Version : YOLO Version 8

### Custom Training :

![](https://github.com/Srishti002/YOLO-object-detection-with-custom-dataset/blob/main/Screenshot%202025-03-23%20235753.png)

   
