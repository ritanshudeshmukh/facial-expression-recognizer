# 😄 Facial Expression Recognizer

A real-time facial expression recognition system built with a Convolutional Neural Network (CNN) and OpenCV. The model detects faces via webcam and classifies them into one of **7 emotions** live on screen.

This project is based on the [Kaggle Facial Expression Recognition Challenge](https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge).

---

## 🎭 Recognized Emotions

| Label | Emotion |
|---|---|
| 0 | Angry |
| 1 | Disgust |
| 2 | Fear |
| 3 | Happy |
| 4 | Sad |
| 5 | Surprise |
| 6 | Neutral |

---

## 📁 Project Structure

```
facial-expression-recognizer/
│
├── Facial-Expression-Recognition-Challenge.ipynb  # Model training notebook
├── model.py                                        # FacialExpressionModel class
├── camera.py                                       # Real-time webcam inference
├── face_model.json                                 # Saved model architecture
├── face_model.h5                                   # Saved model weights
└── haarcascade_frontalface_default.xml             # OpenCV Haar cascade for face detection
```

---

## 🧠 How It Works

1. **Face Detection** — OpenCV's Haar Cascade (`haarcascade_frontalface_default.xml`) detects faces in each webcam frame.
2. **Preprocessing** — The detected face region is cropped, converted to grayscale, and resized to **48×48** pixels.
3. **Emotion Prediction** — The preprocessed face is passed through the CNN, which outputs one of the 7 emotion labels.
4. **Overlay** — The predicted emotion label and a bounding box are drawn on the live video feed.

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/ritanshudeshmukh/facial-expression-recognizer.git
cd facial-expression-recognizer
```

### 2. Install Dependencies

```bash
pip install numpy keras tensorflow opencv-python pandas jupyter
```

### 3. Run Real-Time Detection

Make sure your webcam is connected, then run:

```bash
python camera.py
```

Press **`Esc`** to quit the live feed.

---

## 🏋️ Training the Model

To retrain the model from scratch:

1. Download the dataset from [Kaggle](https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data).
2. Update the dataset path in the notebook.
3. Run all cells in `Facial-Expression-Recognition-Challenge.ipynb`.

The trained model will be saved as `face_model.json` (architecture) and `face_model.h5` (weights).

---

## 🔧 Dependencies

- Python 3.x
- NumPy
- Keras + TensorFlow
- OpenCV (`cv2`)
- Pandas
- Jupyter Notebook

---

## 📄 License

This project is open source. Feel free to fork, explore, and build on it.
