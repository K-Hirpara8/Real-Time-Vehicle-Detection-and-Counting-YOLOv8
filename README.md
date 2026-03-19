# Real-Time Vehicle Detection and Counting using YOLOv8

## 📌 Overview

This project implements a real-time vehicle detection and counting system using a pre-trained YOLOv8 object detection model. Vehicles are detected from video streams and tracked across frames using centroid-based matching.

The goal of this project was to gain hands-on experience in integrating object detection models into a complete computer vision workflow.

---

## 🧠 Model Approach

- A pre-trained YOLOv8 model is loaded using the Ultralytics framework.
- Each video frame is processed independently.
- Bounding boxes are generated for detected vehicles.
- The centroid of each detection is calculated.
- Objects are matched across frames using distance-based comparison.
- A virtual line-crossing logic is applied to count vehicles.

---

## ⚙️ Implementation Details

- Real-time frame processing using OpenCV
- YOLOv8 inference integration in Python
- Centroid-based tracking logic
- Distance threshold matching for object ID consistency
- Line-crossing based counting mechanism

The implementation focuses on clarity and understanding rather than building a production-level tracking system.

---

## 📊 Results & Observations

- The YOLOv8 model provided stable vehicle detection on traffic videos.
- Detection stability influenced counting accuracy.
- Distance threshold tuning improved tracking consistency.
- Runtime performance depends on video resolution and hardware capability.

This project helped me understand practical challenges in combining detection and lightweight tracking methods.

---

## 🖼 Example Inference

After loading the model, the system:

- Captures video frames
- Detects vehicles in each frame
- Assigns temporary object IDs
- Checks if vehicles cross predefined virtual lines
- Updates the vehicle counter in real time

This demonstrates how object detection can be extended into applied computer vision tasks.

---

## 📂 Project Structure

    ├── VehicleDetection.ipynb
    ├── counting.py
    ├── data.yaml
    ├── README.md
    ├── requirements.txt

---

## 🛠 Technologies Used

- Python
- Ultralytics YOLOv8
- PyTorch
- OpenCV
- NumPy

---

## 📥 Installation

Install required libraries:

    pip install -r requirements.txt

---

## ▶️ Running the Project

Run the script:

    python counting.py

Press `q` to exit the video window.

---

## 🎯 What I Learned

- Integrating YOLOv8 with OpenCV for real-time inference
- Implementing centroid-based object tracking
- Handling frame-by-frame video processing
- Designing line-crossing logic for counting
- Understanding trade-offs between accuracy and runtime performance
