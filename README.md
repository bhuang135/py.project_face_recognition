# Face Recognition and Detection with OpenCV

This repository contains Python scripts for implementing face detection and recognition using OpenCV. The project leverages Haar cascades for face detection and provides functionality for capturing and recognizing faces for security applications.

---

## Features
- **Face Detection**: Detect faces in real-time using OpenCV and Haar cascades.
- **Face Recognition**: Compare captured faces with authorized faces for access control.
- **Face Capture**: Capture and store user faces for creating an authorized user database.

---

## File Descriptions

### 1. **face_recognition.py**
   - Performs real-time face recognition.
   - Compares live face data with a pre-saved database of authorized faces.
   - Outputs a success message if the face matches, otherwise denies access.
   - Includes a fallback mechanism for creating a lock file if recognition fails.

### 2. **opencvfacedetection_security.py**
   - Captures face images from a live camera feed and saves them locally.
   - Allows creation of a database of authorized faces for future recognition.
   - Saves up to 100 face images per user with a unique user ID.

### 3. **haarcascade_frontalface_default.xml**
   - A pre-trained Haar cascade file used for face detection.
   - Ensures reliable and accurate detection of frontal faces.

---

## How to Use

### Prerequisites
1. Install Python (version 3.7 or later).
2. Install required dependencies:
   ```bash
   pip install opencv-python numpy
   ```

### Step 1: Setup
- Clone the repository:
  ```bash
  git clone https://github.com/your-username/face-recognition-opencv.git
  cd face-recognition-opencv
  ```
- Ensure the `haarcascade_frontalface_default.xml` file is in the correct directory for OpenCV to load it.

### Step 2: Face Capture
- Run the `opencvfacedetection_security.py` script to capture face images:
  ```bash
  python opencvfacedetection_security.py
  ```
- Enter a unique user ID, and the script will save face images to the `authorized_faces` folder.

### Step 3: Face Recognition
- Run the `face_recognition.py` script to start real-time face recognition:
  ```bash
  python face_recognition.py
  ```
- Look into the camera to verify access.

---

## Folder Structure
```
face-recognition-opencv/
├── face_recognition.py
├── opencvfacedetection_security.py
├── haarcascade_frontalface_default.xml
├── authorized_faces/   # Stores authorized face images
```

---

## Key Notes
- Press `q` to quit any script in real-time camera mode.
- Ensure proper lighting and a clear camera view for best results.
- Modify `similarity` thresholds in the scripts if recognition accuracy needs tuning.

---

## Future Enhancements
- Add support for multi-face recognition.
- Integrate with external APIs for real-time alerts or logging.
- Expand to include deep learning-based face recognition for higher accuracy.

---

## License
This project uses the Haar Cascade XML file provided under the OpenCV license. Please ensure compliance with the licensing terms when redistributing this repository.

---

## Author
- **Your Name**
- [GitHub Profile](https://github.com/your-username)

Enjoy exploring facial recognition with OpenCV!
