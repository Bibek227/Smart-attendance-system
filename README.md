# Face Recognition Attendance System

This project implements a smart attendance system using face recognition. The system captures images, identifies faces using the k-Nearest Neighbors (k-NN) algorithm, and records attendance automatically. The system also integrates a simple Streamlit dashboard to display attendance data in real-time.

## Table of Contents
- [Project Overview](#project-overview)
- [Usage](#usage)
- [How It Works](#how-it-works)

## Project Overview

The Face Recognition Attendance System uses:
- **OpenCV** for image capture and face detection
- **k-NN classifier** (from scikit-learn) for face recognition
- **Streamlit** for displaying real-time attendance data
- **CSV** for recording attendance

## Usage

1. **Add Faces**: First, run the `add_faces.py` script to add new faces to the system.
2. **Take Attendance**: Next, run the `test.py` script to start the face recognition and attendance recording process.
3. **View Attendance**:
   - You can view attendance data in real-time on a web-based dashboard by running the `app.py` script (using Streamlit).
   - Alternatively, you can open the attendance CSV file directly in any spreadsheet application like Excel.

## How It Works

1. **Data Collection**:
    - The system captures face data through a webcam and stores it in a matrix.
    - It collects 100 face images for each person, resizing them to 50x50 pixels.
    - The face data and corresponding names are saved using pickle files.
    
2. **Training**:
    - The system uses the stored face data to train a k-NN model, which is used to predict and recognize faces in real-time.
    
3. **Attendance Recording**:
    - Once a face is recognized, the system records the name and the timestamp in a CSV file.
    
4. **Real-Time Attendance Dashboard**:
    - A Streamlit application reads the CSV file and displays the current attendance with the ability to auto-refresh.



