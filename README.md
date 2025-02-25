# Human Gait Recognition for Security Systems

## Overview

This project presents a human gait recognition system designed for security applications in high-traffic areas such as airports and train stations. The system employs biometric gait analysis to identify individuals based on their unique walking patterns without requiring direct interaction or consent.

## Features

- **Unobtrusive Identification**: Works without user cooperation.
- **Real-time Multi-Person Tracking**: Utilizes YOLOv8 for object detection and Deep SORT for tracking.
- **Gait Energy Image (GEI) Processing**: Condenses gait cycles into single images for efficient recognition.
- **Machine Learning Classification**: Compares extracted gait features with a reference database.
- **High Accuracy**: Achieves up to 98% recognition rate on benchmark datasets.

## Methodology

1. **Human Tracking**

   - Uses YOLOv8 for detecting individuals in a video stream.
   - Deep SORT assigns unique IDs to track people across frames.

2. **Gait Feature Extraction**

   - Converts detected persons into silhouette images.
   - Removes irrelevant details like clothing to focus on body movements.

3. **Gait Recognition Using GEIs**

   - Creates Gait Energy Images (GEIs) from silhouette frames.
   - Captures both static (body shape) and dynamic (movement) information.

4. **Classification**

   - Compares extracted features with a reference database.
   - New features are stored as unknown if no match is found.

## Datasets Used

- **CASIA-C Dataset**
- **Outdoor Gait Dataset**

## Experimental Results

The system was tested on multiple datasets, achieving:

- **CASIA-C**: 94.1% accuracy
- **Outdoor Dataset**: 96-97.7% accuracy
- **Real-world dataset**: 98% accuracy

## Installation

### Prerequisites

- Python 3.x
- OpenCV
- PyTorch
- NumPy
- TensorFlow (if applicable)

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/mohamedsalama677/Gait-recognition.git
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the tracking and recognition script:
   ```bash
   python main.py
   ```

## Applications

- **Surveillance Systems**: Enhancing security in public places.
- **Forensic Investigation**: Identifying individuals in crime scenes.
- **Smart Access Control**: Restricting entry based on gait recognition.

## Limitations & Future Work

- **Challenges**: Viewpoint dependency, environmental variations, and accuracy improvements.
- **Future Enhancements**: Integration with multi-biometric systems, deep learning model refinement, and real-time optimization.

## Contributors

- Mohamed Salama ([GitHub](https://github.com/mohamedsalama677))

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

For further details, go to the [project paper](https://drive.google.com/file/d/1bj3b7fN4Oz6MkvgxWXNT6KU6jHRXx0r7/view?usp=sharing).

