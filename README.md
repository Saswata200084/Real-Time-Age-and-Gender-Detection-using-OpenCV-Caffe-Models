# 🎯 Real-Time Age and Gender Detection using OpenCV & Caffe Models

This project performs real-time **Age** and **Gender** prediction using your webcam feed.  
It utilizes **OpenCV's Deep Neural Network (dnn)** module along with **pre-trained Caffe models** for accurate detection.

---

## 📸 Demo

The system:
- Captures frames from your webcam.
- Detects faces in real time.
- Predicts **age group** and **gender** for each detected face.

---

## 🧠 Models Used

- **Face Detector:** `opencv_face_detector.pbtxt`, `opencv_face_detector_uint8.pb`
- **Age Detector:** `age_deploy.prototxt`, `age_net.caffemodel`
- **Gender Detector:** `gender_deploy.prototxt`, `gender_net.caffemodel`

> You can download these from the official OpenCV repository or other open Caffe model sources.

---

## ⚙️ Requirements

Install the dependencies using:

```bash
pip install opencv-python numpy
If you’re running in a headless environment (like a server or cloud instance):

bash
Copy code
pip install opencv-python-headless
🗂️ Project Structure
css
Copy code
AgeGenderDetection/
│
├── age_deploy.prototxt
├── age_net.caffemodel
├── gender_deploy.prototxt
├── gender_net.caffemodel
├── opencv_face_detector.pbtxt
├── opencv_face_detector_uint8.pb
├── main.py
└── README.md
🚀 How to Run
Clone the repository:

bash
Copy code
git clone https://github.com/<your-username>/AgeGenderDetection.git
cd AgeGenderDetection
Place all model files (.prototxt, .caffemodel, .pbtxt, .pb) in the same directory.

Run the project:

bash
Copy code
python main.py
Press 'q' to close the webcam window.

🧩 Code Overview
main.py

Loads pre-trained Caffe models for face, age, and gender.

Reads frames from webcam in real time.

Detects faces and predicts gender and age for each face.

Displays the predictions on the video window.

🧍 Labels Used
python
Copy code
ageList = ['(0-2)', '(4-6)', '(8-12)', '(15-20)', '(25-32)', '(38-43)', '(48-53)', '(60-100)']
genderList = ['Male', 'Female']
🧰 Tools & Technologies
Python 3.x

OpenCV (cv2)

Caffe Pre-Trained Models

Deep Neural Network (dnn) Module

⚠️ Notes
Accuracy depends on lighting and camera quality.

Predictions are approximate.

Works best in well-lit environments.

📜 License
This project is created for educational purposes.
All model rights belong to their respective owners (OpenCV / Caffe community).
