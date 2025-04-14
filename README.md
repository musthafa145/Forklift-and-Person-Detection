# Forklift and Person Detection

![Forklift Detection](https://img.shields.io/badge/Computer%20Vision-Object%20Detection-blue)
![YOLOv8](https://img.shields.io/badge/Model-YOLOv8-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

A real-time object detection system trained to identify forklifts and people in various environments, helping to improve workplace safety and prevent accidents.

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Demo](#demo)
- [Installation](#installation)
- [Usage](#usage)
  - [Using Pre-trained Model](#using-pre-trained-model)
  - [Training Your Own Model](#training-your-own-model)
  - [Real-time Detection](#real-time-detection)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Performance](#performance)
- [Contributing](#contributing)
- [License](#license)

## 🔍 Overview

Industrial environments where forklifts and pedestrians share space present significant safety challenges. This project leverages the YOLOv8 architecture to create a real-time detection system that can identify forklifts and people in various environments, providing a foundation for safety monitoring systems.

## ✨ Features

- **Real-time detection** of forklifts and people using webcam or video input
- **High accuracy** detection using YOLOv8 architecture
- **Low latency** processing suitable for safety applications
- **Easy integration** with existing camera systems
- **Cross-platform compatibility** (Windows, Linux, macOS)
- **FPS counter** to monitor performance

## 🎬 Demo

[Include screenshots or GIFs of your system in action]

## 🔧 Installation

1. Clone the repository:
```bash
git clone https://github.com/musthafa145/Forklift-and-Person-Detection.git
cd Forklift-and-Person-Detection
```

2. Create a virtual environment (optional but recommended):
```bash
# For Windows
python -m venv venv
venv\Scripts\activate

# For macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

## 🚀 Usage

### Using Pre-trained Model

The repository includes a pre-trained model file (`best.pt`) that you can use right away:

```python
from ultralytics import YOLO

# Load the model
model = YOLO('best.pt')

# Run inference on an image
results = model('path/to/image.jpg')

# Display results
results[0].show()
```

### Training Your Own Model

If you want to train the model on your own dataset:

1. Prepare your dataset in YOLOv8 format
2. Use the training script:

```bash
python train.py --data data.yaml --epochs 100 --batch 16
```

### Real-time Detection

For real-time detection using a webcam:

```bash
python webcam_detection.py
```

Press 'q' to quit the application.

## 📊 Dataset

The model was trained on a merged dataset containing:
- The PersonForklift dataset by Hakan Taskiner
- The Forklift dataset by Saharsh Sinha

The combined dataset features various industrial settings with forklifts and people in different poses, lighting conditions, and environments.

## 🧠 Model Architecture

This project uses YOLOv8, the latest version of the YOLO (You Only Look Once) family of models. YOLOv8 offers several advantages:

- Single-stage object detection for faster inference
- State-of-the-art accuracy and speed trade-off
- Advanced backbone network with CSPDarknet
- Improved anchor-free detection heads
- Enhanced training techniques

## 📈 Performance

| Metric | Value |
|--------|-------|
| mAP@0.5 | 0.94 |
| Inference time | ~15ms per frame (RTX 3080) |
| FPS | ~60 (depends on hardware) |

## 👥 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Contact

Project created and maintained by [Musthafa](https://github.com/musthafa145).

For questions or feedback, please open an issue or contact the repository owner.
