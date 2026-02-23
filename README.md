# 🖼️ YOLOv8 Noise Robustness Analysis

This project evaluates how different **image degradation techniques** — including **Gaussian Noise, Salt & Pepper Noise, Speckle Noise, Poisson Noise, Gaussian Blur, and Motion Blur** — impact **YOLOv8n object detection performance**.

The study analyzes how detection accuracy degrades as noise intensity increases.

---

## ⚙️ Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Anand99-rai/YOLO-Noise-Robustness-Study.git
cd YOLO-Noise-Robustness-Study
```

### 2. Create & Activate Virtual Environment

```bash
python -m venv venv
```

Activate it:

**Windows**
```bash
venv\Scripts\activate
```

**Linux / Mac**
```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🚀 Run the Analysis

Open and run the main Jupyter Notebook:

```bash
main.ipynb
```

The notebook will:

- Load the YOLOv8n model  
- Apply selected noise types  
- Perform object detection  
- Compute evaluation metrics  
- Generate robustness comparison plots  

---

## 📈 Outputs

- **Detection Visualization:** Comparison between original and degraded images  

- **Performance Plots:** mAP, Precision, Recall, and F1-score decay under increasing noise levels  

- **Confidence Analysis:** Detection confidence variation across degradation types  

---

## 📊 Insights

- **Gaussian Noise:** Gradual degradation in detection accuracy  

- **Salt & Pepper Noise:** Noticeable instability at moderate-to-high intensities  

- **Speckle Noise:** Affects bounding box localization consistency  

- **Blur Effects:** Reduce sharp feature detection and small object recognition  

Overall, detection performance decreases as degradation intensity increases.

---

## 🤝 Contributing

Contributions are welcome!

1. Fork this repository  
2. Create a new branch  
3. Commit your changes  
4. Push to your branch  
5. Open a Pull Request  

---

## 👤 Author

Anand Kumar Rai   
Computer Vision & Deep Learning  

GitHub:  
https://github.com/Anand99-rai  

---

