
# Human Face Detection

Face recognition is the problem of identifying and verifying people in a photograph by their face. It is
a task that is trivially performed by humans, even under varying light and when faces are changed by
age or obstructed with accessories and facial hair. Nevertheless, it has remained a challenging
computer vision problem for decades until recently.


Deep learning methods can leverage very large datasets of faces and learn rich and compact
representations of faces, allowing modern models to first perform as-well and later to outperform the
face recognition capabilities of humans.


With this project we have implemented the following under the face detection umbrella: Implement
Bounding Box Regression, Facial Landmark Detection, Blur the Face from the Image, Use Real Time
Image Bounding Box. These models have a great significance in various industries including
Automobile, Security Access Control, Healthcare and so on.



## Applications

The application of the face recognition system has reinforced its roles in Deep Learning as much as
it has done in everyday life.

Social Media: The very first place to go when looking at machine applications is social media. This
is because it is the place where computers and humans meet. On social media, the face recognition
model has been deployed in FaceTune, SnapChat, DeepFace, and even TikTok.

Security and Verification: Another case that the face recognition model is applied is in FaceID
verification. Used especially for security and authentication, you'd find its application on your
smartphone (popularly the recent models of iPhone), CCTV, and other login and unlocking devices
and platforms.

Other Applications: Face recognition systems have been used to identify subjects in photographs, as
access control in security systems, and to scan people's faces in a concert. It has witnessed the most
formal applications to the most informal. Not to be too oblivious, national security agencies like the
FBI have face recognition in their basic toolkit. 


## System Design

The model used for this project is MTCNN. The MTCNN is popular because it achieved then stateof-the-art results on a range of benchmark datasets, and because it is capable of also recognizing
other facial features such as eyes and mouth, called landmark detection. The network uses a cascade
structure with three networks; first the image is rescaled to a range of different sizes (called an
image pyramid), then the first model (Proposal Network or P-Net) proposes candidate facial
regions, the second model (Refine Network or R-Net) filters the bounding boxes, and the third
model (Output Network or O-Net) proposes facial landmarks.

![image](https://user-images.githubusercontent.com/87512533/204122300-e44d7ec1-37d3-41ff-ae79-10fe94f3d1ff.png)



## Functions

1.Bounding Box Regression:
Here we define a function which will draw the given box on the basis of the Coordinates we get from the MTCNN Detector. We use this Function on the Filename and the
Number of Faces as we can see in the end of the code. 

![image](https://user-images.githubusercontent.com/87512533/204122311-8b5e2e42-cbb3-4a72-9bfe-9e4896fb4782.png)


2.Facial Landmark Detection: In this we draw the given facial landmarks and mark them in the way
we want to which are given by the MTCNN Constructor. We draw the given Landmarks which are
Eye’s , Mouth and Nose. We Draw them with given Red Circles as shown in the Output in the
previous Slide. This can be done for multiple faces in a given image and does take a little time but
has a good accuracy.

![image](https://user-images.githubusercontent.com/87512533/204122320-2c3394e6-4080-40e1-9686-8b53a679bee7.png)


3.Blurring Face: We Use the BLUR Function in Open CV in the code. We Blur the Face and this may
have different used applications such as Privacy Preservation.

![image](https://user-images.githubusercontent.com/87512533/204122336-a0b08e7e-fe10-448f-924b-5f7ab4364cbb.png)


4.Real Time Image Bounding: We use this to open our own Laptop’s Camera using OPEN CV and
then putting the real time Images through the MTCNN Constructor and giving us back the
bounding BOX on our given Face infront of the Camera in Real Time.


## Future Plans
Next steps for this project can be to uniquely identify a person from an image source. Crossreference a detected face from a given database of identified faces to get information about the
person in an image. Further, we can use the above model to create a face detection system that
identifies a person in real-time or through video sources.
