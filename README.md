# 🚗 AI-Powered Driver Drowsiness Detection System

An end-to-end AI-powered Driver Drowsiness Detection System that monitors a driver's alertness in real time using Computer Vision and Deep Learning. The system detects prolonged eye closure and yawning through two independently trained CNN models, computes a dynamic drowsiness score, and triggers an alert whenever signs of fatigue are detected.

The project combines image processing, facial landmark detection, deep learning inference, and an interactive dashboard to provide a complete real-time driver monitoring solution.

---

## 📌 Features

- 👁️ Real-time Eye Closure Detection using CNN
- 😮 Real-time Yawn Detection using CNN
- 📹 Live Webcam Monitoring
- 🙂 Facial Landmark Detection using dlib (68 landmarks)
- 📊 Dynamic Drowsiness Score Calculation
- ⏱️ Eye Closure Timer
- 🚨 Automatic Alarm on Drowsiness Detection
- 📈 Interactive Streamlit Dashboard
- 🧩 Modular Project Structure

---

## 🛠️ Tech Stack

- Python
- TensorFlow / Keras
- OpenCV
- dlib
- NumPy
- Streamlit
- Browser-based Audio Alert

---

## 📂 Project Structure

```text
AI_Drowsiness_Detection/
│
├── app.py
├── requirements.txt
├── README.md
│
├── datasets/
├── models/
├── notebooks/
├── src/
```

---

## 🚀 Project Workflow

```text
Webcam
   │
   ▼
OpenCV
   │
   ▼
dlib Face Detection
   │
   ▼
68 Facial Landmarks
   │
   ├───────────────┐
   ▼               ▼
Eye Crop      Mouth Crop
   │               │
   ▼               ▼
Eye CNN       Yawn CNN
   │               │
   └───────┬───────┘
           ▼
Drowsiness Score
           ▼
Alarm Trigger
           ▼
Streamlit Dashboard
```

---

## 📊 Dashboard

The dashboard displays:

- Live Webcam Feed
- Eye Status
- Yawn Status
- Drowsiness Score
- Eye Closure Timer
- Alarm Status
- Session Timer

---

## 🎯 Model Details

### Eye Closure Detection
- Model: CNN
- Classes:
  - Open Eye
  - Closed Eye

### Yawn Detection
- Model: CNN
- Classes:
  - Yawn
  - No Yawn

---

## 📈 Drowsiness Score

The score is calculated using:

- Eye Closure Duration
- Yawn Detection
- Blink Pattern (Optional)

Based on the score:

| Score | Status |
|-------|---------|
| 0-25 | Alert |
| 26-50 | Mild Fatigue |
| 51-75 | Drowsy |
| 76-100 | Critical |

---

## 📦 Installation

```bash
git clone https://github.com/yourusername/AI_Drowsiness_Detection.git

cd AI_Drowsiness_Detection

pip install -r requirements.txt

streamlit run app.py
```

---

## 🔮 Future Improvements

- Head Pose Estimation
- Blink Rate Analysis
- Driver Identification
- Cloud Deployment
- Fatigue Analytics
- Mobile Deployment

---

## ⭐ Acknowledgements

This project was developed as a real-time Computer Vision and Deep Learning application to demonstrate practical AI techniques for driver safety and fatigue monitoring.
