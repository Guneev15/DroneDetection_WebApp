# Drone Detection System using YOLOv8

This project is a **real-time drone detection system** built using **YOLOv8** and a custom-trained model. The system can detect drones in video feeds and provides real-time monitoring statistics. The application is developed with Flask for the backend and a responsive web interface to visualize detections.

## Table of Contents
- [Features](#features)
- [Demo](#demo)
- [Installation](#installation)
- [Usage](#usage)
- [Model Training](#model-training)
- [Acknowledgments](#acknowledgments)

---

## Features
- **Real-Time Drone Detection**: Detects drones in real-time using a trained YOLOv8 model.
- **Live Video Feed**: Streams the live feed for real-time monitoring.
- **Detection Statistics**: Displays session duration, detection rate, and average confidence.
- **Responsive Web Interface**: Built with HTML, Tailwind CSS, and JavaScript, designed for intuitive user experience.

## Demo
A sample screenshot of the detection interface:

![Drone Detection System Interface](screenshot.png)

## Installation
### Prerequisites
- Python 3.7+
- Flask
- OpenCV
- PyTorch
- YOLOv8

### Setup Instructions
1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/drone-detection-system.git
   cd drone-detection-system
   ```

2. **Install Required Packages**
   ```bash
   pip install -r requirements.txt
   ```

3. **Download or Link Model Weights**
   Place the YOLOv8 model weights (e.g., `yolov8n_trained.pt`) in the project directory. Ensure the model file path in the code matches this location.

## Usage
1. **Start the Flask Server**
   ```bash
   python app.py
   ```

2. **Access the Web Interface**
   Open a web browser and navigate to:
   ```
   http://127.0.0.1:5000
   ```

3. **End the Session**
   Click on the **End Session** button to save statistics and shut down the server.

## Model Training
The YOLOv8 model was trained on over 1000 images for drone detection accuracy. To retrain or improve the model:
1. Collect and annotate new drone images.
2. Use the YOLOv8 training script:
   ```python
   yolo train data=data.yaml model=yolov8n.pt epochs=50
   ```
3. Replace `yolov8n_trained.pt` with your newly trained weights.

## File Overview
- `app.py`: Backend logic using Flask to handle video feed, detections, and session management.
- `index.html`: Frontend interface for displaying the video feed, detection results, and session statistics.
- `yolov8n_trained.pt`: Pre-trained model weights for YOLOv8 to detect drones.

## Acknowledgments
Special thanks to my project team members **Bhavishya Singla** and **Arpit Yadav** for their contributions to the development and testing of this project.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contact
For any questions, please feel free to reach out via LinkedIn or GitHub!

---

This should provide all necessary details for users to understand, set up, and run your drone detection system!
