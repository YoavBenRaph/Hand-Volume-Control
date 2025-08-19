# Gesture Volume Control

## 🖐️ Gesture-Based Volume Control with OpenCV & MediaPipe

- Control your system volume using hand gestures captured via webcam! This project uses **MediaPipe** for hand tracking and **Pycaw** to interface with the system's audio settings.

## 🎯 Features

- Real-time hand tracking using webcam
- Detects thumb and index finger distance to control volume
- Visual feedback with FPS and volume bar
- Smooth interpolation between hand distance and system volume

## 🛠️ How It Works

This project combines computer vision and audio control to create a touchless volume interface:

- Hand Detection: Uses MediaPipe to detect and track hand landmarks in real time.
- Gesture Recognition: Tracks the position of the thumb tip (landmark 4) and index finger tip (landmark 8).
- Distance Measurement: Calculates the Euclidean distance between these two points to determine the gesture size.
- Volume Mapping: Uses NumPy's interp() function to map the hand distance to a system volume range.
- System Volume Control: Interfaces with Pycaw to set the master volume level based on the mapped value.
- Visual Feedback: Displays the current volume level, a volume bar, and FPS directly on the webcam feed using OpenCV.

## 📦 Requirements

Make sure you have the following Python libraries installed:

- Opencv-python
- Mediapip
- Pycaw
- Numpy
