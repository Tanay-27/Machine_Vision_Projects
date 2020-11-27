# Machine Vision 
Machine vision (MV) is the technology and methods used to provide imaging-based automatic inspection and analysis for such
applications as automatic inspection, process control, and robot guidance, usually in industry.
#### This Repository contains several small machine vision projects from beginer to intermediate stage. Jupyter notebook is being attached. These are under process of being hosted using flask heroku platform for common use and test.
## Projects Included:-
- Smile detection
- Facial Recognition
- Gaze Detection
- Air Canvas
- Drowsiness Detection
- Invisibility Cloak
- Distance Estimation

## Haar Cascades
Haar Cascade classifiers are an effective way for object detection. This method was proposed by Paul Viola and Michael Jones in their paper Rapid Object Detection using a Boosted Cascade of Simple Features. Haar Cascade is a machine learning-based approach where a lot of positive and negative images are used to train the classifier.
These are XML files containing feature information which are comapred to find the match of various features in the given image.
A lot of projects make use of Haar Cascades. 
#### Another file used for comparision is from the DLIB library "shape_predictor_68_face_landmarks.dat" which works similar to Haar Cascades.

## Smile Detection 
This project uses Haar Cascade Classifiers to detect the smile from the given ROI.
A frame is sent to the `smiledetect()` function where first the faces are searched, if found a blue box is drawn around it.
The region of each face is given to process whether a person is smiling or not, if person is smiling, a red box is drawn around the lips.

## Facial Recogntion 
This project uses face_recognition library and frontal face xml file cloned directly from opencv repo
In this project, the facial encodings are procured from each known face and stored in an array,
These faces along with the label are compared for the encodings for each unknown face and the best match is displayed
This project does not use Machine learning due to the use case having lack of images to train from
This project enables comparision from as low as 1 image to recognise a face

## Air Canvas
This is a complete usable end product used to draw on the screen using a blue coloured dot. This is especially helpfull in the recent times as teachers face difficulty in explaining certain concept due to lack of blackboard. 
In this project the given frame is searched for the blue coloured object, the contour is found, some morphological operations are performed to make the area smooth, the center of that object is considered as a marker and the movement in corrdinates in each successive frame is joined continuously and added to a blank mask and displayed.
User also has the option to chose different colours.

## Drwonsiness Detection
This project can be used by people who drive for long distances especially on highways. This continously tracks the eye and if the eye is closed for more than a pre determined amount of times issues a siren and alerts the user, that he/she may have dosed off.
This calculates what is known as the eye aspect ratio, which is the ratio of the length of the eye to the width of the eye, the coordinates for the eye maximas are found using `dlib`. 
When the eye is open the length from top to bottom of eye will be quite larger than when it is closed. This concept is used to determine whether a person is asleep or not

## Invisibility Cloak
This project tries to replicate the invisibility cloak from the Harry Potter Series using computer vision.
Initially the background frame is taken as reference, then the user may come into the vision of the camera after 1-2 seconds.
The project is set to detect red coloured objects. One may use blanket and as the person covers themself with the red balnket they find that they have been hidden from the view on screen.
This is done by detecting the red colour part and removing the part from each frame and replacing it with the background by ANDING with the compliment of the first mask.

## Distance Estimation
Using this project one can find the estimated distance from the camera of an object by just giving 1 reference image at known distance and width of the object.
The object of detection here is a circle which is being detected using Hough Transform. Hough Transform visualises an image in Parametri or Hough Space and calculates the polar coordinates of the shape under detection. Once the object (here- cicle) is detected, it estimates the distance by comparing its width in pixels to the reference image. The formula used is:-
` (knownWidth * focalLength) / pixelWidth `
Focal length is calculated as ` focalLength = (reference_width * KNOWN_DISTANCE) / KNOWN_WIDTH ` 
Thus by using just a single refernce image the distance can be measured upto a cm accuracy.

## Credits
- https://www.geeksforgeeks.org/
- https://pythonprogramming.net/
- https://towardsdatascience.com/
- https://livecodestream.dev/post/2020-05-26-hough-transformation/
- https://www.pyimagesearch.com
##### Please note - The code has been well commented and efforts have been taken to make it self explanatory, if any queries arise...one can email them to `tanayshah027@gmail.com`
