# EmotionSense
EmotionSense is an innovative application designed to assist healthcare professionals in understanding and interpreting the emotional states of their patients. Utilizing advanced natural language processing (NLP), file analysis capabilities, and real-time camera detection.

[![MIT License](https://img.shields.io/badge/Code-Private-green.svg)](https://github.com/SonuKumar-dev/EmotionSense.git) 

## Tech Used
[![Python](https://img.shields.io/badge/Python-3.11-DA552F.svg?style=for-the-badge&logo=python&logoColor=orange)](https://www.python.org/)
[![Python](https://img.shields.io/badge/Open-CV-7EBC6F.svg?style=for-the-badge&logo=opencv&logoColor=green)](https://opencv.org/)
[![Python](https://img.shields.io/badge/Firebase-Latest-FFCA28.svg?style=for-the-badge&logo=firebase&logoColor=yellow)](https://firebase.google.com/)
[![Python](https://img.shields.io/badge/Machine-Learning-CB171E.svg?style=for-the-badge&logo=uml&logoColor=red)](https://aws.amazon.com/machine-learning/)
[![Python](https://img.shields.io/badge/NLP-Language-FF4B4B.svg?style=for-the-badge&logo=joomla&logoColor=pink)](https://aws.amazon.com/what-is/nlp/#:~:text=Natural%20language%20processing%20(NLP)%20is,manipulate%2C%20and%20comprehend%20human%20language.)

## Library 

[![MIT License](https://img.shields.io/badge/Deepface-0.0.85-green.svg)](https://github.com/serengil/deepface) is a Python library for facial recognition and facial attribute analysis. It seems to be used for some part of the application's functionality related to facial analysis.

[![MIT License](https://img.shields.io/badge/Dlib-19.24.2-red.svg)](https://pypi.org/project/dlib/) is a modern C++ toolkit containing machine learning algorithms and tools for creating complex software in C++ to solve real-world problems. Here, it's used for face detection.

[![MIT License](https://img.shields.io/badge/Joblib-1.3.2-yellow.svg)](https://pypi.org/project/joblib/) Joblib is a library for efficiently saving and loading Python objects (such as machine learning models) to/from disk. Here, it is used to load a pre-trained machine learning model (emotion_model.pkl) for predicting emotions.

[![MIT License](https://img.shields.io/badge/Tkinter-latest-orange.svg)](https://docs.python.org/3/library/tkinter.html) is a standard GUI (Graphical User Interface) library for Python. It is used to create the main window, buttons, text entry fields, etc., providing the user interface for the application.

[![MIT License](https://img.shields.io/badge/CV2-4.9.0.80-pink.svg)](https://pypi.org/project/opencv-python/) is a library of programming functions mainly aimed at real-time computer vision. In this code, it's used for capturing video from the webcam, detecting faces, and drawing on the video frames.

[![MIT License](https://img.shields.io/badge/Pyrebase-4.9.0.80-voilet.svg)](https://pypi.org/project/pyrebase5/) is a Python wrapper for the Firebase API. It is used here for authentication and storage functionalities with Firebase.

[![MIT License](https://img.shields.io/badge/Matplotlib-3.8.3-lightgreen.svg)](https://pypi.org/project/matplotlib/) is a plotting library for Python. It is used here to generate visualizations, such as probability plots.

[![MIT License](https://img.shields.io/badge/sklearn-1.4.1-blue.svg)](https://pypi.org/project/scikit-learn/) to build a text classification model pipeline using logistic regression. It preprocesses the data, trains the model, evaluates its accuracy, and saves it as a serialized file.

[![MIT License](https://img.shields.io/badge/ReportLab-latest-lightorange.svg)](https://pypi.org/project/reportlab/) is used to dynamically generate a PDF document containing information about a patient's report, including the doctor's name, date and time, patient data, and an image (plot).

## Features:
- Textual Emotion Analysis:
    EmotionSense employs advanced NLP algorithms to analyze text inputs provided by patients. This feature extracts nuanced insights into their emotional states, enabling healthcare providers to gain deeper understanding and empathy towards their patients' feelings and concerns.
- File Upload for Comprehensive Analysis:
    Healthcare professionals can upload various types of files, such as documents, images, or audio recordings, for in-depth emotion analysis. This functionality enhances versatility and facilitates a thorough examination of emotional cues across different modalities.
- Real-time Camera Detection:
    EmotionSense offers live emotion detection using the device's camera. By capturing real-time facial expressions and body language, it provides instantaneous feedback on the emotional state of the patient. This dynamic feature enables healthcare providers to gauge patient emotions during consultations or therapy sessions effectively.
- Ease of Access:
    EmotionSense is readily available and easy to use for healthcare providers.
- Simple Design:
    A simple and intuitive design enhances usability by making EmotionSense easy to navigate and understand. 


## 🔭 Installation
#### Pre-Requirement

```bash
- Windows / Linux
- Pycharm
- Python
- Firebase
```

## 🔧 Local development
#### Frontend 

```bash
# clone the repository
https://github.com/SonuKumar-dev/EmotionSense.git

# cd in the project directory
$ cd EmotionSense/

# Install all Requirement
$ pip install -r requirements.txt

# Configure Firebase
- https://console.firebase.google.com/
- create a project and copy the firebaseConfig
- Now add in the auth.py  

# Run the application
$ python app.py

```
#### Backend

```bash
# Configure Firebase
- https://console.firebase.google.com/
- create a project then add web app
- Then From Build select 
  -- Authentication
  -- Storage
  -- Realtime Database

- add rule in Realtime Database in firebase console
{
  "rules": {
    ".read": "now < 1712169000000",  // 2024-4-4
    ".write": "now < 1712169000000",  // 2024-4-4
       "users": {
      "$user_email": {
        "patients": {
      "$phone_number":{
          }
        }
      }
    }
  }
}

- then copy the firebaseConfig 
  firebaseConfig = {
  'apiKey': "",
  'authDomain': "",
  'databaseURL': "",
  'projectId': "",
  'storageBucket': "",
  'messagingSenderId': "",
  'appId': ""
}

- Now add in the auth.py  

```
## Running Demo Video
![](testvideo.gif)

## Results:
Upon analysis, EmotionSense generates detailed patient profiles, including:

- Emotion Score: Indicates the intensity of various emotions exhibited by the patient.
- Predominant Emotion(s): Identifies the primary emotional state(s) present in the patient.

## 🐞Feedback / Issues

If you have any feedback, please reach out to us at @rocksonu12345@gmail.com

## 🙏Special Thanks
[![Python](https://img.shields.io/badge/Python-3.11-DA552F.svg?style=for-the-badge&logo=python&logoColor=orange)](https://www.python.org/)

[![Python](https://img.shields.io/badge/Open-CV-7EBC6F.svg?style=for-the-badge&logo=opencv&logoColor=green)](https://opencv.org/)

[![Google-Fonts](https://img.shields.io/badge/Google-Fonts-8C4FFF.svg?style=for-the-badge&logo=adobefonts&logoColor=white)](https://getbootstrap.com/)

[![All Contributors](https://img.shields.io/badge/All-Contributors-0B996E.svg?style=for-the-badge&logo=bitrise&logoColor=white)]()

