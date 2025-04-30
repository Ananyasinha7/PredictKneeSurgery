# 🦵 PredictKneeSurgery

**PredictKneeSurgery** is an AI-powered tool designed to predict the necessity of knee surgery based on both patient input (age, gender, BMI) and knee X-ray images. The model utilizes **ResNet18** for image classification to assess the severity of osteoarthritis and provides **GradCAM** visualizations to highlight affected regions in the knee. While still under development, this tool provides a foundation for future advancements in osteoarthritis prediction and surgery decision support.

**Colab Link: https://colab.research.google.com/drive/1fWD9lJ8hLxlekxSx50ghxbsLZJhp_-jf#scrollTo=_xk-hR5wjQ4W**

---

## 🚀 Features

- 🔬 **Severity Classification**: Uses **ResNet18** to analyze knee X-ray images and classify the severity of osteoarthritis.
- 🧑‍⚕️ **Heuristic Inputs**: Incorporates user-provided heuristic values such as **BMI**, **age**, and **gender** to make more informed surgery predictions.
- 🌍 **GradCAM Visualization**: Visualizes regions of the knee affected by osteoarthritis using **GradCAM** to highlight areas of concern in the X-ray image.
- ⚖️ **Surgery Prediction**: Combines the results from heuristic values and image analysis to predict if knee surgery is likely required.
- 🏗️ **Under Development**: The model is still in the early stages and provides predictions with **lesser accuracy** for now, but is expected to improve with more training data and fine-tuning.

---

## 🧠 Tech Stack

- **Model**: ResNet18 for image classification (pretrained on ImageNet, fine-tuned on knee X-ray dataset)
- **Visualization**: GradCAM for visualizing areas of osteoarthritis in knee X-rays
- **Heuristic Model**: Uses **BMI**, **age**, and **gender** for preliminary assessment
- **Backend**: Flask for API serving
- **Frontend**: (optional) Can integrate with a web frontend for easier user interaction (under development)
- **Libraries**: PyTorch, OpenCV, Matplotlib, NumPy

---

## 🛠️ How It Works

1. **Input Phase**: 
   - Users input their **age**, **gender**, and **BMI**.
   - Users upload a knee **X-ray image** of the affected knee.
   
2. **Heuristic Assessment**:
   - The input values are processed to calculate risk factors based on BMI, age, and gender.
   
3. **Image Analysis**:
   - The **ResNet18 model** processes the X-ray image and classifies it based on osteoarthritis severity (e.g., mild, moderate, severe).
   - The **GradCAM** visualization technique is used to highlight the regions of the knee affected by osteoarthritis.

4. **Surgery Prediction**:
   - The system combines the **heuristic values** and **knee osteoarthritis severity classification** to predict the necessity of knee surgery.

5. **Output**:
   - The model predicts whether surgery is recommended based on the severity level and input data.
   - GradCAM will display a visual heatmap of the affected areas in the X-ray.

---

## 📦 Setup Instructions

### 1. Clone the Repo

```bash
git clone https://github.com/your-username/PredictKneeSurgery.git
cd PredictKneeSurgery
