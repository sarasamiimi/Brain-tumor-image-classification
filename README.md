# Brain-tumor-image-classification

Brain Tumor Image Classification

lightweight deep-learning web app for MRI tumor detection

This project uses a fine-tuned VGG19 model to classify brain MRI images into two categories:
“Yes Brain Tumor” or “No Brain Tumor.”
A small Flask web app is included so users can upload an image and instantly get a prediction.


-----------------------------------------------------------------------------------------------------

What This Project Does

Loads a pretrained VGG19 network and adds custom dense layers for classification

Processes MRI images automatically (resize → normalize → predict)

Provides an easy-to-use web interface for uploading images

Returns a clear text result—no complications


------------------------------------------------------------------------------------------------
 
 
 Model Summary

Input: 240×240 RGB MRI image

Base model: VGG19 (without top layers)

Custom layers:

Flatten

Dense (4608, ReLU)

Dropout (0.2)

Dense (1152, ReLU)

Output: Dense (2, Softmax)

Weights are loaded from vgg_unfrozen.h5

 How the Web App Works

The Flask app has two simple routes:

/ → Shows the upload page

/predict → Handles the uploaded file and returns the prediction

Behind the scenes, the image is resized, converted to an array, fed into the model, and mapped to a label.




 Getting Started

Install dependencies:

pip install -r requirements.txt


Run the application:

python app.py


Then open your browser and go to:

http://127.0.0.1:5000/

--------------------------------------------------------------------------------------

 Built With

Python

TensorFlow / Keras

Flask

OpenCV

PIL
