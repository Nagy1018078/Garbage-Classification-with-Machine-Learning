# Garbage Classification System

## Overview

This project is a garbage classification system that uses machine learning to categorize images of waste into different classes.  It's designed to help improve waste management processes by automating the identification of different types of garbage.

## Features

* **Image Upload:** Users can upload images of garbage via drag-and-drop or file selection.
* **Classification:** The system uses a pre-trained deep learning model (CNN-RNN) to classify the uploaded image.
* **Results Display:** The application displays the predicted garbage class, confidence level, and class probabilities.
* **Error Handling:** The system provides user-friendly error messages for invalid file types and classification issues.

## Technologies Used

* **Machine Learning:** PyTorch (for model training)
* **Model Architecture:** CNN-RNN (Convolutional Neural Network and Recurrent Neural Network)
* **Hyperparameter Tuning**: Optuna
* **Image Processing:** PIL (Python Imaging Library)
* **Deployment:** Dash

## Model Details

The system uses a hybrid CNN-RNN architecture:

* **CNN (EfficientNet):** Extracts spatial features from the input image.
* **RNN (GRU):** Processes the feature sequence from the CNN to capture contextual information.

The model was trained on a dataset of garbage images and optimized using Optuna for hyperparameter tuning.

## Setup

### Prerequisites

* Python 3.x
* PyTorch
* Optuna

### Installation

1.  **Clone the repository:**

    ```bash
    git clone <https://github.com/Nagy1018078/Garbage-Classification-with-Machine-Learning>
    cd Garbage-Classification-with-Machine-Learning

    ```

2.  **Set up the Python environment (for model training and evaluation - if you need to retrain or evaluate):**

    ```bash
    conda create -n garbage_env python=3.9  # Or: python -m venv garbage_env
    conda activate garbage_env           # Or: source garbage_env/bin/activate
    pip install -r requirements.txt
    ```

The application will be accessible at `http://localhost:8050` (or the address shown in your terminal).
