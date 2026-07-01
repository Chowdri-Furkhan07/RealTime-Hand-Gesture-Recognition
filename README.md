# 🖐️ RealTime Hand Gesture - Controlled Brightness Adjuster

> A touchless Human-Computer Interaction (HCI) system that uses computer vision to detect hand landmarks in real time and dynamically adjusts screen brightness based on finger distance - no physical contact required.

![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green?style=flat&logo=opencv)
![MediaPipe](https://img.shields.io/badge/MediaPipe-Hands-orange?style=flat)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-F37626?style=flat&logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-lightgrey?style=flat)

---

## 📌 Overview

Traditional brightness controls require physical interaction with a keyboard or touchpad. This project eliminates that need by leveraging **real-time hand gesture recognition** through a standard webcam.

Using **MediaPipe's Hand Landmark Detection** and **OpenCV** for video processing, the system tracks the positions of the thumb tip and index finger tip. The **Euclidean distance** between these two landmarks is calculated per frame and mapped to the system's brightness range (0–100%) using **NumPy interpolation**, allowing fluid and responsive brightness control with just a pinch gesture.

---

## ✨ Features

- 🎥 **Real-time webcam-based hand detection** at high FPS
- 👆 **21-point hand landmark tracking** via MediaPipe Hands
- 📐 **Euclidean distance calculation** between thumb and index finger tips
- 🔆 **Dynamic screen brightness mapping** using `numpy.interp()`
- 🖼️ **Live visual feedback** - landmarks, connecting lines, and brightness level rendered on screen
- 🚫 **Zero physical contact** - fully touch-free interaction
- 💻 **Cross-platform compatible** (Windows, macOS, Linux)

---

## 🧠 How It Works

```
Webcam captures live video frames
          ↓
OpenCV reads and flips each frame
          ↓
MediaPipe Hands detects 21 hand landmarks
          ↓
Thumb Tip (landmark 4) & Index Tip (landmark 8) coordinates extracted
          ↓
Euclidean distance calculated between the two points
          ↓
Distance mapped to brightness range [0, 100] using np.interp()
          ↓
screen_brightness_control sets system brightness in real time
          ↓
Visual overlays drawn on frame - landmarks, line, and brightness %
```

**Core Gesture:**

| Gesture | Action |
|---|---|
| 👌 Fingers pinched (close together) | Brightness → Minimum (0%) |
| ✌️ Fingers spread wide apart | Brightness → Maximum (100%) |
| 🤏 Fingers partially open | Brightness → Proportional value |

---

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| Video Capture & Processing | OpenCV (`cv2`) |
| Hand Landmark Detection | MediaPipe Hands |
| Distance & Mapping | NumPy |
| Brightness Control | Screen Brightness Control (`screen_brightness_control`) |
| Development Environment | Jupyter Notebook |
| Language | Python 3.x |

---

## 📁 Project Structure

```
RealTime-Hand-Gesture-Recognition/
│
├── app.py
├── requirements.txt
├── Hand Gesture.ipynb     # Main notebook - full implementation
└── README.md
```

---

## ⚙️ Setup & Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Chowdri-Furkhan07/RealTime-Hand-Gesture-Recognition.git
cd RealTime-Hand-Gesture-Recognition
```

### 2. Install Dependencies

```bash
pip install opencv-python mediapipe numpy screen-brightness-control
```

> **Note (Linux users):** `screen_brightness_control` may require additional permissions. Run with `sudo` or configure udev rules for `/sys/class/backlight/`.

### 3. Run the Notebook

Launch Jupyter and open `Hand Gesture.ipynb`:

```bash
jupyter notebook "Hand Gesture.ipynb"
```

Run all cells - your webcam will activate and brightness control will begin in real time.

**To exit:** Press `q` in the OpenCV window.

---

## 📦 Dependencies

```
opencv-python
mediapipe
numpy
screen-brightness-control
```

---

## 🔑 Key Concepts Demonstrated

| Concept | Implementation |
|---|---|
| Computer Vision | Real-time webcam frame processing with OpenCV |
| Pose/Landmark Estimation | MediaPipe Hands — 21 3D hand landmarks |
| Signal Mapping | `numpy.interp()` for distance-to-brightness mapping |
| System Integration | OS-level brightness control via `screen_brightness_control` |
| HCI Design | Touchless, gesture-driven device interaction |

---

## 💡 Use Cases

- ♿ **Accessibility** - hands-free control for users with motor impairments
- 🏥 **Hygiene-sensitive environments** - hospitals, labs, food prep areas
- 🎮 **HCI Research** - gesture-based UI prototyping
- 🤖 **Smart Home / IoT** - gesture integration with smart lighting systems
- 📚 **Education** - demonstrates real-world CV + ML applications

---

## 🔮 Future Enhancements

- [ ] Extend gesture vocabulary - volume control, media playback, scrolling
- [ ] Multi-hand support for simultaneous controls
- [ ] GUI dashboard showing real-time brightness slider
- [ ] Export gesture logs for behavioral analysis
- [ ] Integration with smart home APIs (Home Assistant, Google Home)
- [ ] Optimize FPS with GPU acceleration (CUDA-enabled OpenCV)

---

## 👤 Author

**Chowdri Furkhan**

Artificial Intelligence & Machine Learning

[![GitHub](https://img.shields.io/badge/GitHub-Chowdri--Furkhan07-181717?style=flat&logo=github)](https://github.com/Chowdri-Furkhan07)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
