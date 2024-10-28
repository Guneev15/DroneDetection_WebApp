Drone Detection System using YOLOv8
This project is a real-time drone detection system built using YOLOv8 and a custom-trained model. The system can detect drones in video feeds and provides real-time monitoring statistics. The application is developed with Flask for the backend and a responsive web interface to visualize detections.

Table of Contents
Features
Demo
Installation
Usage
Model Training
Acknowledgments
Features
Real-Time Drone Detection: Detects drones in real-time using a trained YOLOv8 model.
Live Video Feed: Streams the live feed for real-time monitoring.
Detection Statistics: Displays session duration, detection rate, and average confidence.
Responsive Web Interface: Built with HTML, Tailwind CSS, and JavaScript, designed for an intuitive user experience.
Demo
A sample screenshot of the detection interface:


Installation
Prerequisites
Python 3.7+
Flask
OpenCV
PyTorch
YOLOv8
Setup Instructions
Clone the Repository

bash
Copy code
git clone https://github.com/your-username/drone-detection-system.git
cd drone-detection-system
Install Required Packages

bash
Copy code
pip install -r requirements.txt
Download or Link Model Weights Place the YOLOv8 model weights (e.g., yolov8n_trained.pt) in the project directory. Ensure the model file path in the code matches this location.

Usage
Start the Flask Server

bash
Copy code
python app.py
Access the Web Interface Open a web browser and navigate to:

arduino
Copy code
http://127.0.0.1:5000
End the Session Click on the End Session button to save statistics and shut down the server.

Model Training
The YOLOv8 model was trained on over 1000 images for drone detection accuracy. To retrain or improve the model:

Collect and annotate new drone images.
Use the YOLOv8 training script:
python
Copy code
yolo train data=data.yaml model=yolov8n.pt epochs=50
Replace yolov8n_trained.pt with your newly trained weights.
File Overview
app.py: Backend logic using Flask to handle video feed, detections, and session management.
index.html: Frontend interface for displaying the video feed, detection results, and session statistics.
yolov8n_trained.pt: Pre-trained model weights for YOLOv8 to detect drones.
Acknowledgments
Special thanks to my project team members Bhavishya Singla and Arpit Yadav for their contributions to the development and testing of this project.

License
This project is licensed under the MIT License. See the LICENSE file for more details.
