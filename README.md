# Brain Tumor Detection Using Deep Learning on MRI Images

This project provides a web-based system for detecting brain tumors from MRI images using a deep learning model. The application leverages a neural network trained on MRI scans to identify the presence and type of tumor, and delivers an easy-to-use interface for uploading images and viewing predictions.

## Features

- *Deep Learning Model*: Utilizes a trained Keras/TensorFlow model for accurate tumor detection.
- *Web Interface*: User-friendly web app built with Flask and Bootstrap for uploading MRI images and viewing results.
- *Multiple Tumor Types*: Detects and classifies images as pituitary, glioma, meningioma, or no tumor.
- *Confidence Score*: Displays the model’s confidence in its predictions.
- *Image Handling*: Uploaded images are processed, stored, and results are shown alongside the image.

## Demo

![Screenshot of Web Interface](screenshot.png) <!-- Add a screenshot if available -->

## Getting Started

### Prerequisites

- Python 3.7+
- pip

### Installation

1. *Clone the repository*
    bash
    git clone https://github.com/Avijit-Giri/Brain_Tumour_Detection.git
    cd Brain_Tumour_Detection
    

2. *Install dependencies*
    bash
    pip install -r requirements.txt
    

3. *Model Weights*
   - Ensure the model file is present at models/model.h5.
   - If not, train your model or obtain the weights as per your use case.

### Running the Application

bash
python main.py


- Open your browser and navigate to http://127.0.0.1:5000/
- Upload an MRI image to receive a tumor detection result and confidence score.

## Project Structure


├── main.py             # Main Flask application
├── models/
│   └── model.h5        # Trained Keras/TensorFlow model
├── templates/
│   └── index.html      # Web interface template
├── uploads/            # Stores uploaded images
├── requirements.txt    # Python dependencies
└── README.md


## How It Works

- *Upload*: User uploads an MRI scan via the web interface.
- *Preprocessing*: The image is resized and normalized as required by the model.
- *Prediction*: The model predicts whether the scan shows a tumor, and if so, its type.
- *Result*: The result (tumor type or no tumor) and confidence score are displayed, along with the uploaded image.

## Model Details

- The model is a convolutional neural network (CNN) trained on labeled MRI images.
- Class labels: pituitary, glioma, meningioma, notumor.
- The model outputs both the class (type of tumor or no tumor) and a confidence score.

## Example

- *Input*: MRI image file (PNG, JPG, etc.)
- *Output*:  
    
    Tumor: glioma
    Confidence: 97.34%
    
    or
    
    No Tumor
    Confidence: 99.12%
    

## Acknowledgements

- MRI images dataset: [Kaggle Brain Tumor Dataset](https://www.kaggle.com/datasets/awaiskaggler/brain-tumor-dataset) or similar sources.
- Keras, TensorFlow, Flask, Bootstrap.

## License

This project is licensed under the MIT License.

---

*Maintainer:* [Avijit-Giri](https://github.com/Avijit-Giri)