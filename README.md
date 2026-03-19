# 🚗 Real-Time Vehicle Detection and Counting using YOLOv8

## 📌 Overview

This project implements a real-time vehicle detection and counting system using a YOLOv8 object detection model. Vehicles are detected from a video stream and tracked across frames using centroid-based matching. The system counts vehicles entering and leaving the scene using virtual line-crossing logic.

The objective was to combine detection, lightweight tracking, and counting into a complete computer vision workflow.

---

## ⚙️ How It Works

- A trained YOLOv8 model is loaded using Ultralytics.
- Each frame of the video is processed for vehicle detection.
- Bounding boxes are drawn around detected vehicles.
- The centroid of each bounding box is calculated.
- A distance-based matching function keeps object IDs consistent across frames.
- When a vehicle crosses predefined lines, the counter updates.

---

## 🧠 Tracking Logic

Each detected vehicle is assigned an ID.  
Current centroids are compared with previous frame centroids.  
If the distance between centroids is below a defined threshold, the object keeps the same ID.  
Movement direction determines whether a vehicle has entered or left the scene.

This keeps the implementation simple while maintaining stable counting performance.

---

## 📂 Project Structure

    ├── counting.py
    ├── data.yaml
    ├── README.md
    ├── requirements.txt

---

## 🛠 Technologies Used

- Python
- Ultralytics YOLOv8
- OpenCV
- NumPy
- PyTorch

---

## 📥 Installation

Install required libraries:

    pip install -r requirements.txt

---

## ▶️ How to Run

Update the video path inside `counting.py`, then run:

    python counting.py

Press **q** to exit the video window.

---

## 🎯 What I Learned

- Integrating YOLOv8 with OpenCV for real-time inference  
- Implementing centroid-based multi-object tracking  
- Handling frame-by-frame video processing  
- Designing line-crossing logic for counting  
- Balancing detection performance and runtime efficiency  

---

## 📦 requirements.txt Content

Create a file named `requirements.txt` and add:

    ultralytics
    opencv-python
    numpy
    torch
