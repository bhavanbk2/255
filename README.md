LungNet: Deep Learning Approach for Thoracic Disease Classification
Aradhya Alva Rathnakar, Bhavan Kumar Basavaraju, Mahamaya Panda, Shashi Kumar Kadari Mallikarjuna

How to Run the LungNet Segmentation and Ensemble Classification Models:

Prerequisites
Before running the LungNet models, ensure you have the following installed:
Python 3.8 or higher
TensorFlow 2.x
Keras
NumPy
Pandas
Matplotlib
Scikit-image
Scikit-learn

Installation:
Clone the Repository:
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name

Set Up a Virtual Environment (Optional but recommended):
python -m venv lungnet-env
source lungnet-env/bin/activate  # On Windows use `lungnet-env\Scripts\activate`

1. Lung Segmentation Using U-Net:

Data Preparation:
Ensure that your X-ray images and their corresponding mask files are placed in the appropriate directories as specified in the script.

Segmentation Process:

Run the 'Lungnet_1(Unet_implementation).ipynb' file

This script loads the U-Net model, performs segmentation on the provided X-ray images, and saves the segmented masks along with the model.

2. Disease Classification Using Ensemble Model (ResNet 50 + DenseNet 121):

Data Preparation:
Prepare your dataset by ensuring that all images are correctly labeled and formatted. This might involve resizing images and encoding labels.

Training and Evaluation of the Ensemble Model:

Run the 'Lungnet_2(Segmentation+Ensemble).ipynb' file

This script will train the ensemble model on the preprocessed, segmented, and labeled X-ray images. It involves loading the ResNet 50 and DenseNet 121 models, applying the ensemble techniques, and training on your dataset. After training, this script also evaluates the model performance on a test set. The script will output metrics such as accuracy, recall, and F1-score.

Additional Information
Model Configurations:
If needed, adjust model parameters such as the number of epochs, batch size, and learning rates in the configuration section of each script.

Troubleshooting:
If you encounter any issues, check the Python and library versions, ensure all dependencies are installed, and verify that data paths are correctly set in the scripts.

