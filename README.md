# ComputerVision

Notes:
- the .prototxt file contains the model definition and the .caffemodel contains the actual weights for the model. Together, they are used to detect objects in images — in this case faces. You can replace these files with other models trained on various objects and recognize them as well.


Important Links:

- Deep learning model converter - https://github.com/ysh329/deep-learning-model-convertor
- Facial landmarks with dlib, OpenCV, and Python - https://www.pyimagesearch.com/2017/04/03/facial-landmarks-dlib-opencv-python/
- Image classification with Keras and deep learning - https://www.pyimagesearch.com/2017/12/11/image-classification-with-keras-and-deep-learning/
- Face recognition with OpenCV, Python, and deep learning - https://www.pyimagesearch.com/2018/06/18/face-recognition-with-opencv-python-and-deep-learning/
- Semantic segmentation with OpenCV and deep learning - https://www.pyimagesearch.com/2018/09/03/semantic-segmentation-with-opencv-and-deep-learning/

 

TroubleShooting
- OpenCV: Resolving NoneType errors - https://www.pyimagesearch.com/2016/12/26/opencv-resolving-nonetype-errors/
- Python, argparse, and command line arguments - https://www.pyimagesearch.com/2018/03/12/python-argparse-command-line-arguments/


New Ideas:
- Article on making a “people counting” with OpenCV — that is, a program that counts people going in and out of a building via a live webcam feed. 
- I want to track both hands and face. How to extract the skin tones from the face ? so that I can track the hands : You can detect skin tones but a more robust method would be to use a hand detector, similar to how we detected the face in the image. You could also detect the entire body and then “fit” a skeleton to the body. I’ll be covering that in a future blog post so stay tuned!

New things:
- Is it possible to count the number of people in the screen at the same with this code? (Using a webcam) : Yep. You can create a “counter” variable that counts the total number of faces. Something like:
```
count = 0
...
if confidence > args["confidence"]:
    count += 1
...
```
- If one wants to combine multiple detectors to get a higher accuracy, what approach do you suggest : I’m not sure what you mean by “combine” in this context. Are you referring combining Haar cascades, HOG + Linear SVM, and deep learning-based detectors into a sort of “meta” detector? : You would apply each of them independently and then apply non-maxima suppression. - https://www.pyimagesearch.com/2014/11/17/non-maximum-suppression-object-detection-python/
