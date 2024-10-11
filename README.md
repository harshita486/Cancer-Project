The field of oncology is rapidly evolving with the integration of genetic information into diagnostic and therapeutic frameworks. This project, based on data from the TCGA Pan Cancer analysis project and compiled by the UCI Machine Learning Repository, aims to leverage gene expression profiles to accurately classify tumor samples into one of five cancer subtypes: Breast Invasive Carcinoma (BRCA), Kidney Renal Clear Cell Carcinoma (KIRC), Colon Adenocarcinoma (COAD), Lung Adenocarcinoma (LUAD), and Prostate Adenocarcinoma (PRAD).
The dataset was prudently sampled to ensure sufficient volume for model training while maintaining a size conducive for local and cloud storage. The analysis was bifurcated into unsupervised learning for data relationship exploration and supervised learning for cancer type classification. Unsupervised clustering unveiled intrinsic groupings and potential biomarkers within the genetic data, while supervised learning methods, including Random Forest and KNN, were deployed for predictive modeling. Models were assessed based on their classification reports, with a keen focus on accuracy, precision, recall, and F1 scores across all cancer types.
By confirming the practicality of multiclass classification models in cancer subtype detection. Such technological advancements could eventually lead to improved patient outcomes through more accurate diagnoses and the ability to tailor treatments to the genetic profiles of individual tumors.
The project demonstrated the viability of using machine learning to classify cancer subtypes with high precision. The insights gained from both unsupervised and supervised learning phases have the potential to contribute to personalized cancer diagnostics and targeted treatment strategies


Dataset link
https://drive.google.com/drive/folders/1XMidvlNjYW0KJi7B1ZH4ZbZAyr7E7dap?usp=share_link
import subprocess
import sys

def install(package):
    subprocess.check_call([sys.executable, "-m", "pip", "install", package])

# List of packages to install
packages = ['pandas', 'numpy', 'matplotlib', 'scikit-learn', 'seaborn', 'scipy', 'tensorflow']

for package in packages:
    try:
        dist = __import__(package)
        print("{} ({}) is installed".format(dist.__name__, dist.__version__))
    except ImportError:
        print('{} is NOT installed'.format(package))
        print('Installing...')
        install(package)
        print('{} has been installed'.format(package))
