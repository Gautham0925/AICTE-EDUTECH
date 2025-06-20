# E-Waste Image Classification using EfficientNet – EDUTECH Internship Week 1

## 📍 Project Overview

This project is part of my internship assignment under the **EDUTECH Internship Program (Week 1)**. The primary goal of this project is to build an image classification model that can automatically identify types of **e-waste components** such as mobile phones, keyboards, monitors, etc., using **TensorFlow**, **EfficientNetV2**, and **Keras** on the **Kaggle** platform.

🔗 **Kaggle Notebook**: [View Project Notebook](https://www.kaggle.com/code/gauthampkini/notebooke724678828)

---

## 🎯 What I Understood

Through this project, I gained hands-on understanding of the following concepts:

- How to **organize image datasets** into train/validation/test directories.
- The importance of **data preprocessing** and **augmentation** for better generalization.
- Usage of **transfer learning** with pre-trained models (EfficientNetV2B0 in this case).
- **Model evaluation** using classification reports, confusion matrices, and visual plots.
- **Gradio UI integration** for building an interactive web-based model testing interface (optional due to internet restrictions on Kaggle).
- Handling practical issues such as library installation, kernel limitations, and dataset loading in the Kaggle environment.

---

## 🛠️ Tech Stack & Tools

- **Platform**: [Kaggle Notebooks](https://www.kaggle.com/)
- **Programming Language**: Python 3
- **Libraries/Frameworks**:
  - TensorFlow + Keras
  - NumPy, Matplotlib, Seaborn
  - Scikit-learn
  - PIL (Python Imaging Library)
  - Gradio (for UI, optional)

---

## 📁 Dataset Structure

The dataset was loaded from a Kaggle dataset folder, organized as:

/train/
/keyboard/
/monitor/
/mobile/
...

/val/
/keyboard/
...

/test/
/keyboard/
...


Each subfolder contains labeled images corresponding to its class name.

---

## 🚀 Model Workflow

### Step 1: Data Loading
- Load the dataset using image directory paths.
- Count and display the number of images in each class.
- Visualize class distribution using bar plots.

### Step 2: Preprocessing
- Resize images to `(224, 224)` and apply **EfficientNetV2B0-specific** preprocessing.
- Use `ImageDataGenerator` for rescaling and validation split.

### Step 3: Model Setup
- Load pre-trained `EfficientNetV2B0` without top layer.
- Add custom dense layers and output layer for classification.
- Compile using `Adam` optimizer and `categorical_crossentropy`.

### Step 4: Training
- Train the model using training and validation sets.
- Use `EarlyStopping` and `ModelCheckpoint` for optimization.

### Step 5: Evaluation
- Generate confusion matrix and classification report on test data.
- Plot accuracy and loss curves for training and validation.

### Step 6 (Optional): Gradio Deployment
- Build a simple Gradio interface to upload images and get predictions.
- Internet must be enabled (or run locally) for Gradio to work.

---

## 📊 Sample Output

- Final Accuracy: *95.3*
- Output has been attached within the file

---

## 🧪 Setup Instructions (for Local or Colab)

1. **Dataset**  
   Download the dataset from Kaggle:  
   🔗 [E-Waste Image Dataset – by akshat103](https://www.kaggle.com/datasets/akshat103/e-waste-image-dataset)  

2. **Clone or Download the Notebook**  
You can view or copy the original notebook from Kaggle:  
🔗 [Gautham's Kaggle Notebook](https://www.kaggle.com/code/gauthampkini/notebooke724678828)

3. **Install Required Libraries**  
Run the following in a Colab cell or your local terminal:
```bash
pip install tensorflow gradio matplotlib seaborn scikit-learn pillow

