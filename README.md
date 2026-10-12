# YOLOv8 Real-Time Object Detection

A real-time object detection application built using **YOLOv8 Small, Python, and OpenCV**. The program detects objects through a laptop webcam, displays object names and confidence scores, counts detected objects, and saves the annotated video.

## Features

- Real-time webcam object detection
- Bounding boxes and object labels
- Confidence scores for detected objects
- Total object count and per-class counting
- Live FPS display
- Save annotated video in MP4 format
- Simple keyboard control to stop detection

## Technologies Used

- Python
- YOLOv8 Small (`yolov8s.pt`)
- Ultralytics
- OpenCV
- Computer Vision

## Project Structure

```text
yolov8-live-object-detection/
├── live_detection.py
├── requirements.txt
├── README.md
└── .gitignore
```

## Installation

**1. Install Python**

Install Python and ensure the `py` command works in PowerShell.

**2. Clone the repository**

Replace `YOUR-USERNAME` with your GitHub username.

```bash
git clone https://github.com/YOUR-USERNAME/yolov8-live-object-detection.git
cd yolov8-live-object-detection
```

**3. Install dependencies**

```bash
py -m pip install -r requirements.txt
```

## Run the Project

Start real-time detection using your laptop webcam:

```bash
py live_detection.py
```

The pretrained YOLOv8 Small model is downloaded automatically on the first run if it is not already available.

Press **Q** to stop detection and close the webcam window.

## How It Works

1. Captures live video frames from the webcam.
2. Processes each frame using the YOLOv8 Small model.
3. Detects supported objects above the configured confidence threshold.
4. Draws bounding boxes, object names, and confidence scores.
5. Calculates the total number of detected objects and per-class counts.
6. Displays approximate frames per second (FPS).
7. Saves the annotated video as `live_detection_output.mp4`.

## Supported Objects

The pretrained YOLOv8 model supports 80 standard COCO object categories, including:

- People
- Cars, buses, and bicycles
- Bottles and cups
- Chairs and other furniture
- Laptops and mobile phones

Detection performance depends on lighting, camera quality, object visibility, and computer hardware.

## Output

The application generates an annotated video:

`live_detection_output.mp4`

The video contains the detected object labels, bounding boxes, confidence scores, object counts, and FPS overlay.

## Limitations

- The model may miss small, obscured, or poorly lit objects.
- Performance varies depending on hardware.
- The counter counts detections in each frame; it does not track unique objects across time.
- Custom industrial objects may require a separately trained model.

## Future Improvements

- Object tracking across video frames
- Custom object detection for industrial components
- Detection alerts and event logging
- Performance optimization
- Graphical user interface

## Author

Shaik Ryhan
