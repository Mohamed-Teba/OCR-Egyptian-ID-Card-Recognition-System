# Egyptian ID Card Recognition System 💳✨

**AI-Powered OCR for Egyptian ID Cards – Detect, Extract, Verify!**

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![GitHub]

Welcome to an innovative Python-based solution that leverages AI to detect, process, and verify Egyptian ID cards. Powered by YOLO for object detection, EasyOCR for text recognition, and Streamlit for a slick web interface, this project is your go-to tool for automated ID processing with fraud detection capabilities!

---

## Table of Contents 📑

- [Key Features](#key-features-)
- [How It Works](#how-it-works-)
- [Installation](#installation-)
- [Usage](#usage-)
- [Model Training](#model-training-)
- [Why Choose This System?](#why-choose-this-system-)
- [Acknowledgments](#acknowledgments-)
- [Contributing](#contributing-)
- [License](#license-)
- [Contact](#contact-)

---

## Key Features 🔥

- **AI-Powered ID Detection** 🕵️‍♂️  
  Automatically detects and crops Egyptian ID cards from images using YOLO models.

- **Advanced OCR** 📝  
  Extracts Arabic and English text with high accuracy using EasyOCR, supporting multilingual data extraction.

- **Field Extraction & Data Processing** 📋  
  Captures critical details including:  
  - Full Name  
  - Address  
  - National ID Number  
  - Birth Date  
  - Governorate  
  - Gender  
  - Birth Place  
  - Location  
  - Nationality  

- **Fraud Detection System** 🚨  
  Verifies ID photo authenticity and personal details to flag potential fake IDs.

- **Web Interface with Streamlit** 🌐  
  A sleek, intuitive dashboard for uploading and processing ID cards effortlessly.

---

## How It Works 🛠️

1. **Upload an Image** 📸  
   Drop an Egyptian ID card image into the Streamlit interface.

2. **AI-Powered Detection** 🤖  
   - YOLO detects and crops the ID card.  
   - Specific fields (e.g., name, address) are identified using a custom-trained YOLO model.

3. **Text Extraction** ✂️  
   EasyOCR pulls Arabic and English text from the detected fields.

4. **Data Processing** ⚙️  
   - Extracts key information from the text.  
   - Decodes the National ID to reveal birth date, governorate, and gender.

5. **Fraud Detection** ✅  
   Analyzes the ID photo and details for authenticity, alerting you to potential fraud.

6. **Results Displayed** 📊  
   View structured data and fraud detection status right on the dashboard!

---

## Installation 🚀

Get started in just a few steps:

1. **Clone the Repository**  
   ```bash
   git clone https://github.com/NASO7Y/ocr_egyptian_ID.git
   ```

2. **Navigate to the Project Directory**  
   ```bash
   cd ocr_egyptian_ID
   ```

3. **Create a Virtual Environment** (Recommended)  
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

4. **Install Dependencies**  
   ```bash
   pip install -r requirements.txt
   ```

5. **Run the Application**  
   ```bash
   streamlit run app.py
   ```

**Prerequisites**: Python 3.8+, Git, and a compatible GPU (optional but recommended for faster processing).

---

## Usage 🎮

1. Launch the app with `streamlit run app.py`.
2. Open your browser at `http://localhost:8501`.
3. In the sidebar, upload an Egyptian ID card image (supported formats: jpg, png, etc.).
4. Watch the magic happen as the system processes the image and displays extracted data!

**Example Output**:  
- Full Name: أحمد محمد  
- National ID: 12345678901234  
- Birth Date: 1990-05-15  
- Governorate: Cairo  
- Gender: Male  

---

## Model Training 🧠

- **YOLO Models**  
  - **ID Card Detection**: Trained using `detect_id_card.pt` on a custom dataset (see [Dataset Link](https://www.kaggle.com/datasets/mg31415/synthetic-egyptian-id-cards/data)).  
  - **Field Detection**: Fine-tuned with `detect_objects.pt` for specific ID fields.  
  - Training details are in `yolo_training.ipynb`. Use it to retrain with your own data!

- **EasyOCR**  
  Utilized out-of-the-box for Arabic and English text recognition—no custom training required.

**Tip**: Check out the Jupyter notebook for step-by-step training instructions!

---

## Why Choose This System? 🌟

- **High Accuracy** ✅  
  Cutting-edge YOLO and EasyOCR models ensure precise detection and text extraction.

- **Fraud Detection** 🛡️  
  Built-in verification to catch fake IDs, enhancing security.

- **Fast & Automated** ⚡  
  Say goodbye to manual data entry—process IDs in seconds!

- **User-Friendly** 😊  
  Streamlit’s intuitive interface makes it accessible to everyone.

---

## Acknowledgments 🙌

Big thanks to the amazing tools powering this project:  
- [YOLO](https://github.com/ultralytics/yolov5) – Object detection backbone.  
- [EasyOCR](https://github.com/JaidedAI/EasyOCR) – Text recognition wizardry.  
- [Streamlit](https://streamlit.io/) – Web interface magic.  

---

## Contributing 🤝

We’d love your help to make this project even better!  
1. Fork the repository.  
2. Create a branch for your feature (`git checkout -b feature/cool-idea`).  
3. Commit your changes (`git commit -m "Added cool idea"`).  
4. Push to your branch (`git push origin feature/cool-idea`).  
5. Open a pull request!  

**Ideas Welcome**: Bug fixes, new features, documentation—anything goes!

---

## License 📜

This project is licensed under the MIT License—see the [LICENSE](LICENSE) file for details.