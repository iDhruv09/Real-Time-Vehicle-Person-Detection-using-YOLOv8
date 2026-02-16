# Real-Time-Vehicle-Person-Detection-using-YOLOv8


---

# 🚗 Vehicle & Person Detection in Video using YOLOv8

A deep learning-based computer vision project that performs **object detection on video files** using **YOLOv8**.
The system detects **vehicles and pedestrians**, draws bounding boxes, and displays confidence scores in real-time, generating a processed output video.

Built using **Ultralytics YOLOv8** and OpenCV.

---

## 📌 Project Overview

This project takes a video file as input and:

* 🎯 Detects **persons**
* 🚘 Detects **vehicles** (car, motorcycle, bus, truck)
* 📦 Draws bounding boxes
* 🏷 Displays class names
* 📊 Shows confidence percentage
* 🎥 Saves annotated output video

It uses a pre-trained YOLOv8 model trained on the COCO dataset.

---

## 🧠 How It Works

1. Load YOLOv8 pre-trained model (`yolov8n.pt`)
2. Read input video frame-by-frame
3. Run object detection inference
4. Filter only:

   * Person
   * Car
   * Motorcycle
   * Bus
   * Truck
5. Draw bounding boxes + labels + confidence
6. Save processed frames into a new output video

---

## 🛠️ Tech Stack

* Python
* OpenCV
* YOLOv8
* Deep Learning (Object Detection)
* COCO Pre-trained Model

---

## 📂 Input & Output

**Input:**
`input_video.mp4`

**Output:**
`output_video.mp4`
(With bounding boxes and classification)

---

## 🚀 Installation

```bash
pip install ultralytics opencv-python
```

---

## ▶️ Run the Program

```python
from ultralytics import YOLO

model = YOLO("yolov8n.pt")

model(
    source="input_video.mp4",
    save=True,
    classes=[0,2,3,5,7],  # person + vehicles
    conf=0.25
)
```

Output will be saved automatically inside:

```
runs/detect/predict/
```

---

# 🌍 Real-World Use Cases

This concept is widely used in real-world intelligent systems.

---

## 🚦 1. Smart Traffic Monitoring

* Detect number of vehicles on road
* Monitor congestion levels
* Analyze traffic patterns
* Improve traffic light control systems

Problem Solved:

> Manual traffic monitoring is inefficient and expensive.

---

## 🚘 2. Automatic Vehicle Counting

* Count cars, buses, trucks
* Generate daily traffic reports
* Urban planning analytics

Problem Solved:

> Cities need real-time traffic data for infrastructure planning.

---

## 🚶 3. Pedestrian Safety Systems

* Detect people near roads
* Trigger alerts in autonomous vehicles
* Prevent accidents

Problem Solved:

> Reduce pedestrian accidents using AI detection systems.

---

## 🏢 4. Smart Surveillance Systems

* Detect suspicious activity
* Monitor restricted zones
* Improve security automation

Problem Solved:

> Human-based CCTV monitoring is error-prone and not scalable.

---

## 🚗 5. Autonomous Driving Support

* Object detection is core to self-driving systems
* Detect road participants in real-time

Problem Solved:

> Vehicles need environmental awareness to navigate safely.

---

## 📊 6. Traffic Analytics & Data Science

* Analyze peak traffic hours
* Study vehicle type distribution
* Predict congestion trends

Problem Solved:

> Manual data collection is slow and inaccurate.

---

# 🔥 Why YOLOv8?

* Fast inference speed
* High detection accuracy
* Lightweight versions available
* Easy deployment

---

# 📈 Future Improvements

* Add vehicle counting
* Add object tracking (assign ID per vehicle)
* Speed estimation
* Deploy as web application
* Connect with live CCTV feed
* Store analytics in database
* Train custom dataset

---

# 🎯 Project Highlights

✔ End-to-end video detection pipeline
✔ Real-time object detection
✔ Clean output video generation
✔ Production-ready structure
✔ Scalable to smart city applications

---

# 👨‍💻 Author

Developed as a Computer Vision & Deep Learning project.

---


