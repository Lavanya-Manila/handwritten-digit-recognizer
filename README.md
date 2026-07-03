# Handwritten Digit Recognition using CNN

A deep learning project that recognizes handwritten digits (0–9) using a Convolutional Neural Network (CNN) built with TensorFlow and Keras. The model is trained on the MNIST dataset and achieves approximately **98.98% test accuracy**. In addition to predicting digits from the test dataset, the project allows users to upload their own handwritten digit images for real-time prediction.

---

## Project Overview

Handwritten digit recognition is one of the most popular introductory computer vision problems. In this project, a CNN learns to identify handwritten digits by extracting visual features such as edges, curves, and shapes from grayscale images.

The model is trained using the **MNIST dataset**, which contains 70,000 handwritten digit images.

* **Training Images:** 60,000
* **Testing Images:** 10,000
* **Image Size:** 28 × 28 pixels
* **Classes:** 10 (Digits 0–9)

---

## Features

* CNN-based handwritten digit recognition
* Automatic download of the MNIST dataset
* Image preprocessing and normalization
* Model training with TensorFlow/Keras
* Accuracy and loss visualization
* Confusion Matrix for performance analysis
* Prediction on test images
* Upload custom handwritten images for prediction
* Save and reload trained model using the `.keras` format

---

## Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Matplotlib
* Scikit-learn
* Pillow (PIL)
* Google Colab

---

## Model Architecture

The CNN consists of the following layers:

1. Conv2D (32 filters, 3×3, ReLU)
2. MaxPooling2D (2×2)
3. Conv2D (64 filters, 3×3, ReLU)
4. MaxPooling2D (2×2)
5. Flatten
6. Dense (128 neurons, ReLU)
7. Dense (10 neurons, Softmax)

---

## Data Preprocessing

Before training, the dataset is preprocessed by:

* Scaling pixel values from **0–255** to **0–1**
* Reshaping images from

```
28 × 28
```

to

```
28 × 28 × 1
```

to make them compatible with the CNN input layer.

For uploaded images, the following preprocessing steps are applied:

* Convert image to grayscale
* Resize to 28 × 28 pixels
* Invert colors (if necessary)
* Normalize pixel values
* Reshape for model prediction

---

## Training Configuration

| Parameter           | Value                           |
| ------------------- | ------------------------------- |
| Optimizer           | Adam                            |
| Loss Function       | Sparse Categorical Crossentropy |
| Epochs              | 5                               |
| Batch Size          | Default (32)                    |
| Activation Function | ReLU, Softmax                   |

---

## Model Performance

| Metric        | Value      |
| ------------- | ---------- |
| Test Accuracy | **98.98%** |
| Test Loss     | **0.0304** |

The model demonstrates excellent performance on the MNIST test dataset while maintaining low validation loss.

---

## Evaluation

The project evaluates the trained model using:

* Training Accuracy
* Validation Accuracy
* Training Loss
* Validation Loss
* Test Accuracy
* Confusion Matrix
* Prediction vs Actual Visualization

The confusion matrix provides detailed insight into which digits are classified correctly and highlights the few cases where visually similar digits are misclassified.

---

## Project Workflow

```
Load MNIST Dataset
        │
        ▼
Preprocess Images
        │
        ▼
Build CNN Model
        │
        ▼
Compile Model
        │
        ▼
Train Model
        │
        ▼
Evaluate Performance
        │
        ▼
Visualize Accuracy & Loss
        │
        ▼
Generate Confusion Matrix
        │
        ▼
Save Trained Model
        │
        ▼
Upload Custom Image
        │
        ▼
Preprocess Image
        │
        ▼
Predict Handwritten Digit
```

---

## Sample Prediction

After uploading a handwritten digit image, the model outputs:

```
Predicted Digit: 7
Confidence: 99.87%
```

---

## Project Structure

```
Handwritten-Digit-Recognition/
│
├── digit_recognition_model.keras
├── handwritten_digit_recognition.ipynb
├── README.md
└── sample_images/
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/Handwritten-Digit-Recognition.git
```

Navigate to the project folder:

```bash
cd Handwritten-Digit-Recognition
```

Install the required packages:

```bash
pip install tensorflow numpy matplotlib scikit-learn pillow
```

---

## How to Run

1. Open the notebook in Google Colab or Jupyter Notebook.
2. Run all cells to train the CNN model.
3. Save the trained model.
4. Upload a handwritten digit image.
5. View the predicted digit and confidence score.

---

## Future Improvements

* Interactive drawing canvas for handwritten input instead of image upload
* Data augmentation for improved robustness
* Streamlit web application
* FastAPI backend for deployment
* Docker support
* Model deployment on cloud platforms
* Mobile-friendly interface
* Real-time webcam digit recognition

---

## Learning Outcomes

Through this project, I gained practical experience in:

* Convolutional Neural Networks (CNNs)
* Image preprocessing techniques
* Deep learning model evaluation
* TensorFlow and Keras workflows
* Model serialization and loading
* Confusion Matrix analysis
* Building an end-to-end image classification pipeline

---

## Acknowledgements

* TensorFlow & Keras
* MNIST Handwritten Digit Dataset
* Google Colab

---

## License

This project is licensed under the MIT License.
