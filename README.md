# AI-fitness
Different types of exercises tracked for proper form 

#  AI-Based Full Body Exercise Tracker

[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Platform](https://img.shields.io/badge/Platform-Windows/Linux/Mac-lightgrey.svg)]()
[![Status](https://img.shields.io/badge/Project-Active-brightgreen.svg)]()

This project is an AI-powered fitness tracker that uses computer vision to **track and count multiple bodyweight exercises** such as push-ups, pull-ups, bicep curls, squats, lunges, and shoulder presses in real-time using your webcam. It ensures **only correct form** is accepted, eliminating false counts from improper movements or postures.



##  Features

-  Real-time body pose detection via webcam
-  Accurate rep counting using angle-based motion analysis
-  Filters out false detections due to poor form or non-exercise movements
- On-screen display of reps and form alerts
-  Modular design for each exercise
-  No additional hardware required



## 🏋️‍♂️ Exercises Supported

| Exercise         | Form Detection | Alerts | Rep Counter |
|------------------|----------------|--------|-------------|
| Push-Ups         | ✅             | ✅     | ✅          |
| Pull-Ups         | ✅             | ✅     | ✅          |
| Bicep Curls      | ✅             | ✅     | ✅          |
| Squats           | ✅             | ✅     | ✅          |
| Lunges           | ✅             | ✅     | ✅          |
| Shoulder Press   | ✅             | ✅     | ✅          |



##  Installation

### 1. Clone the Repository

git clone https://github.com/your-username/ai-fitness-tracker.git
cd ai-fitness-tracker

## create the virtual environment
python -m venv venv
source venv/bin/activate  # Linux / Mac
venv\Scripts\activate     # Windows

pip install -r requirements.txt
to run :
python pushups.py          # Push-up tracker
python pullups.py          # Pull-up tracker
python bicep_curls.py      # Bicep curls
python squats.py           # Squat tracker
python lunges.py           # Lunges tracker
python shoulder_press.py   # Shoulder press

Technologies Used

MediaPipe – Real-time pose estimation
OpenCV – Webcam feed and drawing utilities
NumPy – Angle computations

ai-fitness-tracker/
│
├── pushups.py
├── pullups.py
├── bicep_curls.py
├── squats.py
├── lunges.py
├── shoulder_press.py
├── requirements.txt
└── README.md

Contributing
Contributions are welcome! Submit a pull request or open an issue to suggest improvements or new features.

Acknowledgements
Thanks to MediaPipe for the pose estimation models.

Built as part of an effort to combine AI and health-tech.

## 📐 How Angle-Based Tracking Works

Each joint angle is computed using vector trigonometry from 3 key landmarks detected by MediaPipe.

ANGLE EXPLANATION:

def calculate_angle(a, b, c):
    a = np.array(a)
    b = np.array(b)
    c = np.array(c)
    
  radians = np.arctan2(c[1]-b[1], c[0]-b[0]) - np.arctan2(a[1]-b[1], a[0]-b[0])
    angle = np.abs(np.degrees(radians))
    if angle > 180.0:
        angle = 360 - angle
    return angle

##  Contact

Author : Mallikarjun S Y 
📧 Email: your.email@example.com  
🔗 LinkedIn: [YourLinkedInProfile](https://linkedin.com/in/yourname)
