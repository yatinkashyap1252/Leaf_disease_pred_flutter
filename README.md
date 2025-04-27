# Mango Disease Prediction

A Flutter mobile application designed to detect diseases in mango leaves using a machine learning model. This app helps farmers and agricultural enthusiasts identify common diseases affecting mango crops by simply capturing or selecting an image of the leaf.

## Introduction

Mango crops are susceptible to various diseases that can significantly reduce yield and quality. Early detection and diagnosis are crucial for effective treatment and management. This app leverages machine learning to provide a quick and accessible solution for mango disease detection on mobile devices.

## Features

- Capture images of mango leaves using the device camera.
- Select existing images from the device gallery.
- Run on-device inference using a TensorFlow Lite model for fast and offline predictions.
- Display the predicted disease label along with the confidence score.
- User-friendly interface with clear visual feedback.

## How It Works

1. The user opens the app and either takes a photo of a mango leaf or selects one from the gallery.
2. The app loads a pre-trained TensorFlow Lite model and runs the image through it.
3. The model outputs the predicted disease class and confidence level.
4. The app displays the prediction results to the user.

## Model Training

The machine learning model used in this app was created using **Teachable Machine**, a web-based tool by Google that allows users to train custom image classification models without deep expertise in machine learning. The model was trained on a dataset of mango leaf images representing various diseases and healthy leaves.

After training, the model was exported in TensorFlow Lite format (`model_unquant.tflite`) for efficient deployment on mobile devices. The corresponding labels are stored in `labels.txt`.

## Getting Started

### Prerequisites

- Flutter SDK (version 3.7.2 or compatible)
- A physical device or emulator with camera support

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd leaf_disease_pred
   ```

2. Install the required dependencies:
   ```bash
   flutter pub get
   ```

3. Connect your device or start an emulator.

4. Run the app:
   ```bash
   flutter run
   ```

## Project Structure

- `lib/main.dart`: Main Flutter app source code.
- `assets/model_unquant.tflite`: TensorFlow Lite model file.
- `assets/labels.txt`: Labels for the model's output classes.
- `assets/download.png`: Placeholder image shown before any prediction.

## Dependencies

- [flutter_tflite](https://pub.dev/packages/flutter_tflite): For running TensorFlow Lite models on Flutter.
- [image_picker](https://pub.dev/packages/image_picker): For capturing images from camera and selecting from gallery.

## Future Improvements

- Add support for more diseases and larger datasets to improve accuracy.
- Implement real-time camera detection without needing to capture images.
- Provide treatment suggestions based on detected diseases.
- Add multi-language support for wider accessibility.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests for improvements.

## License

This project is licensed under the MIT License.

---

*This app combines the power of Flutter and the simplicity of Teachable Machine to provide an accessible tool for mango disease detection, empowering farmers with technology.*
