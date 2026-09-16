# PEDESTRIAN-DETECTION

## About the Project

This project consists of a computer vision application focused on pedestrian detection in video streams. Developed in Python, the `detector.py` script processes local video files (`walking.avi`) to detect people moving through the scene.

To classify visual elements, the program uses a pre-trained Haar Cascade classifier loaded from an XML file (`fullbody.xml`). The algorithm analyzes the pixel matrices of each video frame to identify patterns and geometric features corresponding to the human body. When a pedestrian is detected, the script dynamically renders a bounding box around the target, adjusting its dimensions according to the detected person's position and size within the frame.

---

## Features

* Structured reading and decoding of digital video streams in `.avi` format.
* Frame-by-frame analysis of pixel matrices using computer vision techniques.
* Automated full-body detection using a Haar Cascade classifier (`fullbody.xml`).
* Real-time rendering of bounding boxes around detected pedestrians.

---

## Technologies Used

* **Python 3**
* **OpenCV** (`cv2`)
* **Haar Cascade** (`fullbody.xml`)

---

## Objective

The main objective of this project is to explore object detection techniques and digital video processing using OpenCV. The technical focus is on understanding Haar Cascade-based detection, loading pre-trained classifiers, processing sequential video frames, and rendering visual detection results over moving image frames.

---

## Learning Outcomes

During the development of this project, the following concepts were applied:

* Using `cv2.CascadeClassifier` to load an external XML file containing a pre-trained detection classifier.
* Implementing `while True` loops to capture and process video frames individually using `cv2.VideoCapture`.
* Applying `detectMultiScale` to extract the Cartesian coordinates ($X, Y$) and dimensions ($W, H$) of detected pedestrians.
* Using `cv2.rectangle` to render bounding boxes around detected objects.
* Managing and releasing video-processing resources using `video.release()` and `cv2.destroyAllWindows()` when execution is complete.

---

## How to Run

1. Make sure Python is installed on your machine.

2. Install the OpenCV dependency:

```bash
pip install opencv-python
```

3. Make sure `walking.avi` and `fullbody.xml` are located in the same directory as the script.

4. Navigate to the project folder:

```bash
cd PEDESTRIAN-DETECTION
```

5. Run the main script:

```bash
python detector.py
```

---

## Project Structure

```text
PEDESTRIAN-DETECTION/
│
├── fullbody.xml
├── detector.py
├── walking.avi
└── README.md
```

---

## License

This project was developed exclusively for educational and learning purposes.

Developed as a hands-on exercise in computer vision and pedestrian detection with Python, applying pixel-matrix processing and bounding-box rendering to local video streams using OpenCV.
