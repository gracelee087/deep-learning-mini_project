# 🧠 Deep Learning Mini Project

## 📌 Project Overview

This project demonstrates how to build a **custom image classifier** using transfer learning.  
A pre-trained **VGG16** model is fine-tuned to classify various real-world object categories captured through webcam images.

---

## 💡 Motivation

In modern computer vision, adapting pre-trained models to real-world data is often more effective than training from scratch.  
In this project, I explored **transfer learning**—specifically VGG16 fine-tuning—to improve accuracy on a manually collected dataset of common objects and stationery.

---

## 📸 Data Collection

Images were captured **manually** using a webcam via the [`imageclassifier`](https://github.com/bonartm/imageclassifier) tool.  
Each image was then **manually sorted** into category folders.

**Target classes included:**

- blue_highlighter
- blue_pen
- eraser
- lotion
- mouse
- multi_color_pen
- oil_based_pen
- pen_refill
- yellow_highlighter

**Folder structure:**

```text
Photo_Collection/
├── blue_highlighter/
├── blue_pen/
├── eraser/
├── lotion/
├── mouse/
├── multi_color_pen/
├── oil_based_pen/
├── pen_refill/
└── yellow_highlighter/
⚠️ Photo_collection contains 230 images for sufficient training data.


🧪 Methodology

• **Environment**: Project runs in a Python virtual environment (`venv`), with dependencies defined in `requirements.txt`  
• **Preprocessing**: Images resized and normalized to fit VGG16 input requirements  
• **Modeling**:  
  - Imported **VGG16** pre-trained on ImageNet  
  - Replaced top layers with custom dense layers  
  - Experimented with freezing/unfreezing base layers  
• **Training**:  
  - Optimizer: Adam  
  - Loss: Categorical Crossentropy  
  - Validation set split to monitor overfitting  
• **Evaluation**: Accuracy metrics and confusion matrix analysis

---

🔬 Key Learnings & Experiments

• Fine-tuning VGG16 layers improved performance significantly over using it as a frozen feature extractor  
• The quality and diversity of images had a major effect on generalization  
• Data augmentation and regularization techniques effectively reduced overfitting

---

📈 Results

| Model Version         | Accuracy (Validation)  |
|-----------------------|------------------------|
| Frozen VGG16          | ~72%                   |
| Fine-tuned VGG16      | **~89%**               |

✅ Transfer learning and fine-tuning led to a **significant performance boost** on webcam-collected real-world data.

---

🧰 Setup Instructions

> For **Windows (Git Bash)**:

```For Git-Bash CLI
python -m venv .venv
source .venv/Scripts/activate
pip install --upgrade pip
pip install -r requirements.txt
jupyter lab

```For PowerShell CLI
pyenv local 3.11.3
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install --upgrade pip
pip install -r requirements.txt

```macOS type
pyenv local 3.11.3
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt


📁 Repository Structure

```text
├── Photo_Collection/          # Collected image data
├── tunning.ipynb              # Main training & evaluation notebook
├── requirements.txt
├── README.md
└── .venv/                     # Python virtual environment (not pushed)

🛠️ Technologies Used

- **Python**, **Keras**, **TensorFlow**
- **OpenCV** – for manual webcam image capture
- **JupyterLab** – for interactive training & prototyping
- **VGG16** – from `keras.applications`
- **Git & GitHub** – for version control and collaboration

🙋🏻‍♀️ Author

**Sohee Lee**  
Aspiring ML Engineer focused on computer vision & deep learning.  

🔗[`GitHub`](https://github.com/gracelee087)
🔗[`LinkedIn`](https://www.linkedin.com/in/soheeleecv/)


