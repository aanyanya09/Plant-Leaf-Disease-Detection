
🌿 Plant Leaf Disease Detection Using CNN
An image-classification project that uses Convolutional Neural Networks (CNNs) to identify a supported plant type and predict the condition of its leaf.

The project is implemented in a Google Colab notebook and uses two CNN models in a two-step prediction workflow.

📌 Project Overview
The system contains two classifiers:

Plant Classifier — predicts one of three plant categories:

Pepper
Potato
Tomato
Plant Disease Classifier — predicts one of the 15 leaf-condition classes represented in the notebook's dataset.

Both models use leaf images resized to 128 × 128 pixels. Image pixel values are normalized before prediction.

✨ Key Features
Trains two separate CNN models.
Classifies leaf images into Pepper, Potato, or Tomato.
Predicts a supported disease or healthy-leaf category.
Displays prediction confidence scores.
Checks plant-classifier confidence before attempting disease prediction.
Compares the plant prediction with the plant associated with the predicted disease class.
Evaluates model performance using test data, classification reports, and a confusion matrix.
Includes example predictions using uploaded leaf images.
🔄 How It Works
The user uploads a leaf image.
The image is resized to 128 × 128 pixels and normalized.
The plant classifier predicts whether the image belongs to Pepper, Potato, or Tomato.
If the plant prediction confidence is below the notebook's 80% threshold, the system reports that the prediction is uncertain.
If confidence is sufficient, the disease classifier predicts a leaf-condition class.
The system checks whether the predicted disease class corresponds to the plant predicted in step 3.
The prediction and confidence scores are displayed.
🧠 Models and Implementation
Framework: TensorFlow / Keras
Model type: Convolutional Neural Network (CNN)
Input image size: 128 × 128 pixels
Batch size: 32
Optimizer: Adam
Loss function: Sparse categorical cross-entropy
Evaluation: Accuracy, classification report, and confusion matrix
The notebook creates and trains both models. The saved model filenames are:

plant_classifier.keras
plant_disease_model.keras
These model files are generated when the relevant notebook cells are run; they are not included in this repository package.

📂 Repository Structure
plant-leaf-disease-detection/
│
├── plant_leaf_disease_detection.ipynb   # Model training, evaluation, and prediction
├── README.md                            # Project documentation
├── requirements.txt                     # Python dependencies
└── .gitignore                            # Files excluded from Git
🗂️ Dataset
The notebook expects the PlantVillage dataset to be available in Google Colab at:

/content/plantvillage
The dataset should be extracted into class-specific folders, with each folder containing images for its class. The notebook loads these folders using TensorFlow's image_dataset_from_directory.

The dataset is not included in this repository. Obtain it from an authorized source and follow its applicable terms of use.

🚀 Run the Project in Google Colab
Open Google Colab.
Upload plant_leaf_disease_detection.ipynb or open it from your GitHub repository.
Make the PlantVillage dataset available at /content/plantvillage, using the folder structure described above.
If you use the notebook's Kaggle authentication setup, add your Kaggle API token to Colab Secrets with the exact name KAGGLE_API_TOKEN.
Run the notebook cells in order.
Train and evaluate the models.
Run the image-upload prediction section to test a leaf image.
Security note: Never upload your Kaggle API token, kaggle.json, passwords, or other credentials to GitHub.

📦 Install Dependencies
For a local Python environment, install the packages listed in requirements.txt:

pip install -r requirements.txt
The notebook uses Google Colab-specific functionality for secret access and file uploads. For the smoothest experience, run it in Google Colab.

👥 Team Members
Purnima
Shashi Pandey
⚠️ Limitations
Predictions are limited to the plant and leaf-condition classes represented in the training dataset.
Image quality, lighting, background, and leaf orientation may affect predictions.
A confidence score is the model's estimated confidence, not a guarantee that the prediction is correct.
This project is an educational machine-learning application and should not replace advice from a qualified agricultural expert.
🔮 Future Improvements
Add support for more plant species and disease categories.
Test the models on leaf images captured in real-world conditions.
Improve generalization using data augmentation and additional training data.
Build a simple web application for easier image upload and prediction.
Project: Plant Leaf Disease Detection Using CNN
Team: Purnima and Shashi Pandey
