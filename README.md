# Drowsiness-Detection
This project is a Drowsiness Detection System that monitors the driver’s facial features to detect signs of drowsiness and alerts the driver when necessary. It uses a computer vision approach by analyzing the eye aspect ratio (EAR) to determine if the driver’s eyes are closing, signaling potential drowsiness. This can help prevent accidents caused by drowsy driving.

Features
Detects face landmarks using dlib's 68-point facial landmark detector.
Computes the Eye Aspect Ratio (EAR) to monitor eye closures.
Triggers an alert with a sound when drowsiness is detected.
Uses OpenCV for real-time video capture and image processing.
Utilizes imutils for easier image transformations.
How It Works
The system calculates the Eye Aspect Ratio (EAR) for both eyes using the landmarks detected around the eyes.
If the EAR falls below a predefined threshold for a consecutive number of frames, the system considers the driver to be drowsy and triggers an alert.
An alarm sound is played to wake up the driver and prevent accidents.
Prerequisites
Before running the project, ensure you have the following installed:

Python 3.x
OpenCV (cv2)
dlib
imutils
scipy
pygame (for audio alerts)
Required Files
shape_predictor_68_face_landmarks.dat: This is the pre-trained model used to detect facial landmarks. You can download it from dlib's model page.
music.wav: An audio file to be played as an alert.
Installation
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/Drowsiness-Detection-System.git
Install the required dependencies:

bash
Copy code
pip install -r requirements.txt
Place the shape_predictor_68_face_landmarks.dat file in the models/ directory.

Ensure music.wav is in the root folder of the project.

Running the Project
To start the drowsiness detection system, run the following command:

bash
Copy code
python Drowsiness_Detection.py
This will start capturing video from your webcam and monitor for signs of drowsiness.

How to Customize
Threshold Tuning: You can change the thresh and frame_check variables to adjust the sensitivity of the drowsiness detection system:
thresh: Controls the EAR value below which the system will detect eye closure.
frame_check: Specifies the number of consecutive frames where the EAR value should be below the threshold before triggering the alert.
Acknowledgments
The project uses dlib's pre-trained 68-point facial landmark detector to identify key facial features.
Audio alert functionality is powered by pygame.
