# Plant Leaf Disease Detection using CNN

A Google Colab/Jupyter notebook project that uses two Convolutional Neural Network (CNN) models:

1. **Plant classifier** — classifies leaf images into Pepper, Potato, or Tomato.
2. **Disease classifier** — classifies images across the 15 dataset categories used by the notebook.

The notebook resizes images to **128 × 128**, normalizes pixel values, trains the models, evaluates them, and includes image-prediction examples.

## Project files

- `plant_leaf_disease_detection.ipynb` — training, evaluation, and prediction notebook.
- `requirements.txt` — Python package dependencies.

## Run in Google Colab

1. Upload `plant_leaf_disease_detection.ipynb` to Google Colab.
2. Make the PlantVillage dataset available at `/content/plantvillage`, matching the directory structure expected by `image_dataset_from_directory`.
3. If using Kaggle to obtain the dataset, add your Kaggle API token to Colab Secrets under the name `KAGGLE_API_TOKEN`. **Never commit API tokens or `kaggle.json` to GitHub.**
4. Run the notebook cells from top to bottom.
5. The notebook saves these trained model files:
   - `plant_classifier.keras`
   - `plant_disease_model.keras`

## Dataset

This repository does not include the PlantVillage image dataset. Download it from its authorized source and place the extracted class folders inside `/content/plantvillage` in Colab.

## Notes

- The notebook expects the dataset folders to be organized by class.
- The two `.keras` model files are generated after training and are intentionally excluded from this source-code package. They can be large; store them separately (for example, in Google Drive or a model-storage service) if needed.
- Model predictions are intended for the dataset's supported plant categories and should not be treated as a substitute for expert agricultural diagnosis.
