# Student-Attention-Detection

AI-based Student Attention Detection using YOLOv8 and MobileNetV2 with Transfer Learning

---

## Problem Statement

With the rapid adoption of digital and hybrid classrooms, instructors lack real-time visual feedback to assess student engagement. Unlike physical classrooms—where facial expressions, eye contact, and posture provide cues—online environments make it difficult to monitor attentiveness at scale.

This project addresses that gap by using computer vision and deep learning to automatically detect and classify students as **Attentive** or **Not Attentive**, enabling objective and scalable classroom monitoring.

---

## Objective

- Detect students in classroom images using object detection  
- Classify each detected student as **Attentive** or **Not Attentive**  
- Provide visual feedback using bounding boxes  
- Convert subjective observation into measurable analytics  

---

## System Overview

The system follows a **two-stage deep learning pipeline**:

### 1. Student Detection (YOLOv8)
- Uses a pre-trained YOLOv8 model  
- Detects multiple students (person class) in a single frame  
- Outputs bounding boxes for each detected individual  

### 2. Attention Classification (MobileNetV2)
- Transfer learning using ImageNet weights  
- Lightweight and efficient CNN  
- Binary classification using sigmoid activation  

---

## Dataset Information

The dataset is sourced from **Roboflow Universe** and contains annotated classroom images representing student attentiveness.

### Original Classes
- Face with eyes open  
- Face with eyes closed  
- Head-down posture  

### Converted Labels
- **Attentive**
- **Not Attentive**

### Dataset Split
- Training: 70%  
- Validation: 15%  
- Testing: 15%  

### Dataset Link
https://universe.roboflow.com/my-model/student-attention-tracking

### License
CC BY 4.0 (Creative Commons Attribution)

---

## Model Performance

### Final Metrics

### Final Metrics

| Metric              | Value   |
|---------------------|---------|
| Training Accuracy   | ~98%    |
| Validation Accuracy | ~95%    |
| Test Accuracy       | ~94.8%  |
| Validation Loss     | ~0.16   |
| Test Loss           | ~0.18   |


The close alignment between validation and test accuracy indicates good generalization and minimal overfitting.

---

## Accuracy and Loss Curves

- **Accuracy vs Epochs**: Training and validation accuracy increase steadily  
- **Loss vs Epochs**: Training and validation loss decrease consistently  

These curves demonstrate stable convergence and effective transfer learning.  


---

## Sample Outputs

- Green bounding box → Attentive  
- Red bounding box → Not Attentive  

The system can detect and classify multiple students simultaneously in a single classroom image.  
Sample output images are available in the `Output/` directory.

---

## Conclusion

This project demonstrates how deep learning can enhance digital education by providing real-time, objective insights into student engagement.  
By combining **YOLOv8** for student detection and **MobileNetV2** for attention classification, the system achieves high accuracy while remaining computationally efficient and scalable.

---

## Future Work

- Extend the model to support multi-level attention classification  
- Perform temporal attention tracking using video streams  
- Develop analytics dashboards for instructors  
- Deploy as a real-time web application


