Classification (Deep Learning)

A complete deep-learning pipeline for classifying brain tumor MRI images.
The system uses VGG19 transfer learning, custom preprocessing, and a Flask web application that allows real-time inference directly from user-uploaded images.



Features

• Full deep-learning workflow
Includes dataset preparation, augmentation, model training, fine-tuning, evaluation, and deployment.

• VGG19 Transfer Learning
A pre-trained VGG19 network is adapted for tumor classification, improving accuracy with limited medical data.

• Real-time Web App (Flask)
Users can upload MRI images through a simple web interface and receive predictions instantly.

• Robust preprocessing pipeline
Images are cleaned, resized, normalized, and augmented for better generalization.

• Reproducible and modular
Training is in a Jupyter notebook, while inference is fully separated in a Flask app.


 
 Project Structure
├── app.py                       Flask web app for real-time prediction  
├── model.h5                     Trained VGG19 model  
├── model_training.ipynb         Training, augmentation, evaluation  
├── static/                       app styling  
├── templates/                     HTML interface  
└── README.md                




 Model Architecture

• Base model: VGG19 (pretrained on ImageNet)
• Layers unfrozen: last convolution block
• Custom classifier head:
– Flatten
– Dense layers with ReLU
– Dropout to reduce overfitting
– Softmax output

The model is optimized using Adam and categorical cross-entropy.


 Training Process

• Data Augmentation:
Random rotations, flips, zoom, brightness shifts

• Training Metrics:
Accuracy, loss curves, confusion matrix (included in notebook)

• Results:
Stable convergence with strong test accuracy for tumor / no-tumor prediction



 How to Run the Web App
1. Install dependencies:
pip install -r requirements.txt

2. Run the Flask app:
python app.py

3. Upload an MRI image

The model returns the predicted class and confidence score.


Example Workflow

Preprocess & clean dataset

Train VGG19 with fine-tuning

Evaluate model with test data

Export .h5 model

Deploy with Flask → lightweight medical inference tool


Why This Project Matters

Medical imaging is one of the toughest real-world ML challenges.
This project shows your ability to:

• Work with imperfect real-world data
• Use advanced deep learning architectures
• Deploy models as usable applications
• Understand evaluation and generalization
• Build a full ML pipeline from zero to deployment
