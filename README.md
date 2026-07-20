<div align="center">

# 😷 Streamlit Face Mask Detector

### A [Streamlit](https://www.streamlit.io/) frontend for face mask detection in images, powered by a pre-trained [Keras](https://keras.io/) CNN model, [OpenCV](https://opencv.org/), and neural network interpretability tools.

<img src="https://github.com/virtualramblas/streamlit-face-mask-detector/raw/master/images/demo_image.PNG" alt="Demo image" width="85%" />

<br/>

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Streamlit](https://img.shields.io/badge/Streamlit-%23FE4B4B.svg?style=for-the-badge&logo=streamlit&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white)
![OpenCV](https://img.shields.io/badge/opencv-%23white.svg?style=for-the-badge&logo=opencv&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)

</div>

---

## 📖 Table of Contents
- [General Info](#-general-info)
- [Deep Learning Explanation](#-deep-learning-explanation)
- [Usage](#-usage)
- [Credits](#-credits)

---

## ℹ️ General Info

This example has been implemented as part of my evaluation of the Streamlit framework. It uses OpenCV to detect faces in the input images and a CNN as a mask/no-mask binary classifier applied to the face ROI.

The Deep Learning model currently used has the architecture suggested by Adrian Rosebrock [here](https://www.pyimagesearch.com/2020/05/04/covid-19-face-mask-detector-with-opencv-keras-tensorflow-and-deep-learning/), and has been trained using [this image data set](https://github.com/prajnasb/observations/tree/master/experiements/data). The trained model has been shared in this repo.

The face detector algorithm comes from [here](https://github.com/Shiva486/facial_recognition): the Caffe model and its descriptor are in the `face_detector` directory.

---

## 🧠 Deep Learning Explanation

Once an image has been uploaded, the classification happens automatically. It is then possible to apply some interpretability methods for neural network understanding. The UI presents two buttons to apply the following methods:

| Method | Description |
|---|---|
| 🔥 **Grad-CAM** | Visualizes how parts of the input image affect a CNN's output by examining the activation maps. |
| 🕶️ **Occlusion Sensitivity** | Visualizes how parts of the input image affect a CNN's confidence by iteratively occluding parts of it. |

---

## 🚀 Usage

**1. Clone this repository**
```bash
git clone https://github.com/virtualramblas/streamlit-face-mask-detector.git
cd streamlit-face-mask-detector
```

**2. Create a virtual environment and install the dependencies**
```bash
pip install -r requirements.txt
```

**3. Run the application**
```bash
streamlit run st_face_mask_detector_expl.py
```

The app will open automatically in your browser — upload an image and the mask/no-mask classification, along with the interpretability visualizations, will be generated on the spot.

---

## 🙏 Credits

- Model architecture inspired by [Adrian Rosebrock's COVID-19 Face Mask Detector](https://www.pyimagesearch.com/2020/05/04/covid-19-face-mask-detector-with-opencv-keras-tensorflow-and-deep-learning/)
- Training data set from [prajnasb/observations](https://github.com/prajnasb/observations/tree/master/experiements/data)
- Face detector (Caffe model) from [Shiva486/facial_recognition](https://github.com/Shiva486/facial_recognition)
- Built with [Streamlit](https://www.streamlit.io/)

<div align="center">

⭐️ If you found this project useful, consider giving it a star!

</div>
