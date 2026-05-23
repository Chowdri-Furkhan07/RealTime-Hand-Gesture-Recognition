# Hand Gesture Recognition System

An AI-powered computer vision application that enables real-time screen brightness control using hand gestures. The project uses OpenCV and MediaPipe to detect hand landmarks and interpret finger movements through a webcam, providing a touch-free and interactive user experience.

## Features

* Real-time hand tracking and gesture recognition
* Touchless screen brightness control
* Accurate finger landmark detection using MediaPipe
* Dynamic brightness adjustment based on finger distance
* Live visual feedback with gesture visualization
* Smooth and responsive user interaction

## Tech Stack

* Python
* OpenCV
* MediaPipe
* NumPy
* Screen Brightness Control (SBC)

## Working Principle

The system captures live video through a webcam and detects hand landmarks using MediaPipe’s Hands module. The distance between the thumb tip and index finger tip is calculated and mapped to the system brightness range using interpolation techniques. As the finger distance changes, the screen brightness is adjusted dynamically in real time.

## Use Cases

* Touch-free system control
* Human-Computer Interaction (HCI)
* Smart automation systems
* Accessibility-focused applications
* Gesture-based device control

## Project Goal

The main objective of this project is to integrate computer vision and gesture recognition technologies to create an efficient, user-friendly, and contactless brightness control system for modern smart environments.
