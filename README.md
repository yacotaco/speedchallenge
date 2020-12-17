Welcome to the comma.ai Programming Challenge!
======

Your goal is to predict the speed of a car from a video.

- data/train.mp4 is a video of driving containing 20400 frames. Video is shot at 20 fps.
- data/train.txt contains the speed of the car at each frame, one speed on each line.
- data/test.mp4 is a different driving video containing 10798 frames. Video is shot at 20 fps.

Ideas to check and explore:
-----

The main idea is to train NN on provided speed data and optical flow images generated from video.
I'm not sure how moving objects (slowing down or speeding up cars) will affect predictions so 
I will try to apply mask and extract spacific region of image/video (unobstructed part of road).
Also lighting conditions across all images need brightness equalization (conversion to HSV).
Check for artifacts and blur.
Maybe combination of above method with inverse perspective mapping (IPM) is worth trying.

update:

What probably would make predictions more accurate is extracting line stripes and dot marks information
from image. Road markings are standardized in terms of size and distance which they have to be placed
from each other. Knowing exact distance traveled and time it is possible to calculate speed. 
Everytime line features are present in image separate model can make correction for optical flow prediction.

Useful links:
-----

Solution
-----
