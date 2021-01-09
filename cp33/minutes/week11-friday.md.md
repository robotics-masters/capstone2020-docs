* Zy has got bounding boxes (circles) around some of the circular signs using OpenCV
    - Parking sign is difficult to detect in this way because it is green with a green background
* It is easy to extract the sign images once the bounding box is placed, allowing for data to be passed into the NN with most of the background noise gone
    - Next step is to retrain model to work using these sorts of images
* Update to brut server hardware occurring soon, should make training extremely fast and allow for multiple groups to train at the same time
* Client demo is planned for 5-7 pm Thursday Week 13 (26/11)