# Biomentric Recognition using Footprints via Siamese Network

A deep learning approach for biometric recognition (identification as well as verification) based on the paper "FootprintNet: a Siamese network method for biometric identification using footprints". It works based on the Triplet Loss method to train the CNN. 

Developed as part of my Project in Networks and Security and basis for my Master's Thesis as the JKU University in Austria. 

## Project Overview
Traditional biometric classifiers only recognize individuals seen during training. This project implements a **Siamese Neural Network architecture** to solve the "open-set problem" for footprint recognition. 

Instead of classifying identities directly, the network maps footprint images into a low-dimensional feature space where relative distances determine whether two footprints belong to the same person.

### Key Features
* **Triplet Loss:** Trains on Anchor, Positive, and Negative image triplets to optimize feature distances.
* **Zero-Retraining Verification:** New individuals can be registered instantly by saving their coordinate vector to a database without retraining the model.
* **Modular Pipeline:** Built with PyTorch and designed for training on Google Colab with GPU acceleration.

## Repository Structure
```
├── src/                  # Core Python modules
│   ├── dataset.py        # Triplet generator (Anchor, Positive, Negative)
│   ├── model.py          # Siamese architecture & Triplet Loss implementation
│   ├── train.py          # Training loop and loss tracking
│   └── evaluate.py       # EER (Equal Error Rate) & ROC curve computation
├── notebooks/            # Google Colab notebooks for training & experiments
├── requirements.txt      # Python dependencies
├── .gitignore            # Excludes heavy datasets and model weights
└── README.md             # Project documentation
```

## Evironment Setup
### 1. Clone Repository
```
git clone [https://github.com/AndyFrosch/footprint_biometrics_master_thesis.git](https://github.com/AndyFrosch/footprint_biometrics_master_thesis.git)
cd footprint_biometrics_master_thesis
```

### 2. Install Dependencies
```
pip install -r requirements.txt
```

## Dataset
Just as in the reference paper, this project uses the public Biometric 220x6 Human Footprint Dataset.

Note: Raw image files and trained model weights (*.pth) are excluded from Git tracking via .gitignore and are stored separately on Google Drive.

## License
This project is open-source under the MIT License.
