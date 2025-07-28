
# 🏛️ Egyptian Monuments Classification with Grad-CAM Bounding Boxes

This deep learning project uses a **Convolutional Neural Network (CNN)** based on **MobileNetV2** to classify 22 iconic **Egyptian monuments** — such as the Sphinx, Pyramids, Nefertiti, Ramesses II, and more.

To enhance explainability, **Grad-CAM** is applied to visualize the model’s attention and generate **bounding boxes** over the most influential image regions. This makes the model interpretable and prepares the dataset for future **YOLO object detection training**.

---

## 📂 Dataset

The dataset is structured with one folder per class and is available on [Kaggle](https://www.kaggle.com/datasets/karimomran/egypt-monuments-dataset):

```
/Data/
    /sphinx/
    /pyramids/
    /nefertiti/
    ...
```

> 📍 The dataset path used in the notebook: `/kaggle/input/egypt-monuments-dataset/Data`

---

## 🧠 Model Summary

- **Base**: MobileNetV2 (pretrained on ImageNet)
- **Architecture**:
  - GlobalAveragePooling
  - Dense(256, ReLU)
  - Dropout(0.3)
  - Output Dense (Softmax for 22 classes)

- **Parameters**:
  - 🧮 Total: `2,591,576`
  - 🔧 Trainable: `2,188,694`

---

## 🔍 Grad-CAM + Bounding Boxes

Grad-CAM is used to extract heatmaps showing where the model is "looking" when making predictions. Then, we extract **bounding boxes** from the heatmap to localize the area of interest — making the model output both **classification** and **localization** insights.

This approach helps in:
- Interpreting model predictions visually
- Generating bounding box data to train object detectors like **YOLO**

---

## 🖼️ Example Output

![Grad-CAM Bounding Box Example](example_output.jpg)

---

## 🚀 How to Run

1. Clone this repository:
```bash
git clone https://github.com/YOUR_USERNAME/egyptian-monuments-cnn-gradcam.git
cd egyptian-monuments-cnn-gradcam
```

2. Upload your dataset to the directory:
```
/Data/
```

3. Open and run the notebook:
```
Egyptian_Monuments_CNN_with_GradCAM.ipynb
```

---

## 🧰 Tech Stack

- TensorFlow & Keras
- MobileNetV2
- Grad-CAM (custom)
- OpenCV
- NumPy, Matplotlib
- Gradio (for UI deployment)

---

## 📎 Related Links

- 📝 [Kaggle Notebook](https://www.kaggle.com/code/belalomran/egyptian-monuments-cnn-with-grad-cam-visualization)
- 🗂 [Kaggle Dataset](https://www.kaggle.com/datasets/karimomran/egypt-monuments-dataset)

---

## 📬 Contact

Feel free to connect or reach out!

- 📧 Email: your.email@example.com  
- 💼 [LinkedIn](https://www.linkedin.com/in/YOURUSERNAME)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## ⭐️ Acknowledgements

- [MobileNetV2](https://arxiv.org/abs/1801.04381)
- [Grad-CAM](https://arxiv.org/abs/1610.02391)
- [Kaggle Dataset by Karim Omran](https://www.kaggle.com/datasets/karimomran/egypt-monuments-dataset)
