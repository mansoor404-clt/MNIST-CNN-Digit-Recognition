# MNIST CNN Digit Recognition

A beginner-friendly convolutional neural network (CNN) that learns handwritten digits from MNIST. Includes a Jupyter notebook for training and evaluation, plus a drawing app that updates its prediction automatically as you draw.

## Features
- TensorFlow/Keras CNN trained on MNIST
- Test evaluation and confusion matrix
- Live prediction and confidence while drawing
- Model saved locally and excluded from Git to keep the repository small

## Project structure
```text
MNIST-CNN-Digit-Recognition/
├── app/digit_recognition.py
├── models/.gitkeep
├── notebooks/MNIST_CNN_Training.ipynb
├── train.py
├── requirements.txt
├── .gitignore
└── README.md
```

## Setup
Python 3.10 or newer is recommended.

```bash
python -m venv .venv
```

Activate it with `.venv\Scripts\Activate.ps1` in Windows PowerShell or `source .venv/bin/activate` on macOS/Linux. Then install dependencies:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## Train
From the project root:

```bash
python train.py
```

The first run downloads MNIST and saves `models/mnist_cnn.keras`. Alternatively, open `notebooks/MNIST_CNN_Training.ipynb` in Jupyter and run its cells.

## Draw and predict
After training:

```bash
python app/digit_recognition.py
```

Draw a digit from 0 to 9 with the mouse. Its prediction and confidence update as you draw. Use **Clear** to start over.

Tkinter is included with many Python installations. Some Linux distributions provide it as a separate system package. MNIST images are centered 28×28 grayscale images, so predictions on differently styled drawings can vary.
