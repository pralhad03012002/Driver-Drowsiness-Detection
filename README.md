# Driver-Drowsiness-Detection
This project uses the dlib facial landmark library and numpy for detecting driver drowsiness on the basis of the distance between the facial landmarks representing the top and bottom of the eyes and the top and bottom of the mouth with a delay function so as to allow for blinking.
Coding Process:
The following illustrates the general idea of the process:
1. The face is captured using the Hog & SVM face detector and then the landmarks are
placed by passing the 68 landmark detector file in the shape predictor function.

2. The eye aspect ratio is calculated using euclidean distances between points, and split
into 3 categories >0.25 which represents an active state, >0.18 & <0.25 which
represents a drowsy state and <0.18 which represents a sleeping state.

3. To avoid blinking being incorrectly recognised as drowsiness, states are only assigned
after 8 consecutive frames of the eye aspect ratio being in the same category.
