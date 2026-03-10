<div align="center">

# 🤟 TradutorDeLibras

### Real-time Brazilian Sign Language (LIBRAS) recognition and translation system

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![MediaPipe](https://img.shields.io/badge/MediaPipe-Latest-00C853?style=for-the-badge&logo=google&logoColor=white)](https://mediapipe.dev)
[![YOLOv11](https://img.shields.io/badge/YOLOv11-Ultralytics-FF6F00?style=for-the-badge)](https://ultralytics.com)
[![FastAPI](https://img.shields.io/badge/FastAPI-Latest-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.x-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)](https://opencv.org)

</div>

---

## 📌 About

**TradutorDeLibras** is an AI-powered system that detects and translates Brazilian Sign Language (LIBRAS) gestures into text in real time. Built as an applied research project at **LAPISCO AI Research Lab (IFCE)**, it combines hand landmark detection with deep learning gesture classification to make communication more accessible for the deaf and hard-of-hearing community.

---

## ✨ Features

- 📸 **Automated Data Collection** — script-based webcam capture to build a custom LIBRAS dataset
- 🤚 **Hand Landmark Extraction** — MediaPipe identifies 21 key hand points per frame for precise gesture mapping
- 🧠 **Deep Learning Classification** — YOLOv11 model trained on LIBRAS gesture data for robust real-time recognition
- 🎥 **Real-time Translation** — live webcam feed with gesture detection and text output
- 🖼️ **Static Image Testing** — support for gesture recognition on individual images
- ⚡ **FastAPI Backend** — lightweight REST API to serve model inference

---

## 🏗️ Architecture

```
Camera Input / Static Image
         │
         ▼
  MediaPipe (Hand Landmark Detection — 21 keypoints)
         │
         ▼
  YOLOv11 (Gesture Classification)
         │
         ▼
  FastAPI (Inference API)
         │
         ▼
  Text Output (Translated Sign)
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Hand Detection | MediaPipe |
| Gesture Classification | YOLOv11 (Ultralytics) |
| Image Processing | OpenCV |
| Backend / API | FastAPI (Python) |
| Numerical Processing | NumPy |

---

## 📂 Project Structure

```bash
├── data/
├── images/
├── collect_imgs.py       # Automated webcam data collection
├── create_dataset.py     # Converts images to hand landmarks
├── training.py           # Model training pipeline
├── testing.py            # Real-time webcam testing
├── testing_imgs.py       # Static image testing
├── model.p               # Trained model
└── data.pickle           # Processed landmark dataset
```

---

## ⚙️ Getting Started

### Prerequisites

```bash
pip install opencv-python mediapipe ultralytics fastapi uvicorn numpy
```

### 1. Data Collection *(optional — skip if using existing dataset)*

```bash
python collect_imgs.py
```

### 2. Create Dataset

```bash
python create_dataset.py
```

### 3. Train the Model

```bash
python training.py
```

### 4. Run Real-time Translation

```bash
python testing.py
```

### 5. Run the API

```bash
uvicorn main:app --reload
```

---

## 🤝 Contributing

Contributions are welcome!
Feel free to open an **Issue** or submit a **Pull Request**.

---

## 📄 License

This project is licensed under the **MIT License**.

---

<div align="center">
Developed by <a href="https://github.com/DerickBessa"><strong>Derick Bessa</strong></a> @ <strong>LAPISCO AI Research Lab</strong>
</div>
