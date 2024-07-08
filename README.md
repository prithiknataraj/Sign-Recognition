# Sign-Recognition

This project implements a real-time hand gesture recognition system using OpenCV, Mediapipe, and machine learning models. The system detects and classifies hand gestures using a webcam and provides audio feedback for recognized gestures.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Model Training](#model-training)
- [Dependencies](#dependencies)
- [Contributing](#contributing)

## Features

- Real-time hand gesture detection and classification.
- Uses OpenCV and Mediapipe for hand landmark detection.
- Classification models for key points and point history.
- Provides audio feedback for recognized gestures.

## Installation

### Prerequisites

- Python 3.x
- Virtual environment (optional but recommended)

### Steps

1. Clone the repository:

```sh
git clone https://github.com/prithiknataraj/Sign-Recognition.git
cd hand-gesture-recognition
```

2. Create and activate a virtual environment:

```sh
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

3. Install the required packages:

```sh
pip install -r requirements.txt
```

## Usage

To run the hand gesture recognition system:

```sh
python main.py --device 0 --width 960 --height 540
```

### Command Line Arguments

- `--device`: Index of the video capture device (default: 0).
- `--width`: Width of the video capture (default: 960).
- `--height`: Height of the video capture (default: 540).
- `--use_static_image_mode`: Use static image mode (default: False).
- `--min_detection_confidence`: Minimum detection confidence (default: 0.7).
- `--min_tracking_confidence`: Minimum tracking confidence (default: 0.5).

## Configuration

You can configure the behavior of the system by modifying the command line arguments or directly editing the `main.py` file.

## Model Training

If you want to train your own models for key point classification or point history classification, you can do so by preparing datasets and following machine learning model training steps. The existing labels are located in the `model/keypoint_classifier` and `model/point_history_classifier` directories.

### Adding New Gestures

To add new gestures:
1. Run the program in logging mode (`mode 1` for keypoints, `mode 2` for point history).
2. Press number keys (`0`-`9`) to record data samples.
3. Train the models with the collected data.

## Dependencies

- OpenCV
- Mediapipe
- Numpy
- Gtts
- Pyttsx3
- Collections
- Csv
- Itertools

Install these dependencies via:

```sh
pip install opencv-python mediapipe numpy gtts pyttsx3
```

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -am 'Add some feature'`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.
