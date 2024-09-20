# Next-Word-Predictor

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Data Preprocessing](#data-preprocessing)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Results](#results)

## Installation
To run this project, ensure you have the following libraries installed:

```bash
pip install numpy pandas tensorflow
```

## Usage
### Clone the repository:
```bash
git clone <repository-url>
cd next-word-predictor
```

### Prepare your dataset:
Place your text dataset in the /kaggle/input/next-word-predictor-data/ directory as dataset.txt.

### Run the model:
Execute the main script to train the model:
```bash
python main.py
```

## Data Preprocessing
The dataset is preprocessed using the following steps:

- Tokenization: The text data is tokenized into sequences using Keras' Tokenizer.
- Padding: Sequences are padded to a maximum length of 86 using pad_sequences.
- One-Hot Encoding: The target words are one-hot encoded for multi-class classification.

## Model Architecture
The model consists of the following layers:

- Embedding Layer: Converts integer sequences into dense vectors of fixed size.
- LSTM Layer: A single LSTM layer with 150 units to capture temporal dependencies.
- Dense Layer: A fully connected layer with softmax activation for multi-class output.

## Training
The model is trained for 100 epochs with the following settings:

- Loss Function: Categorical Crossentropy
- Optimizer: Adam

During training, the model achieved an accuracy improvement from 5.47% to over 93%.

## Results
The model's performance can be evaluated based on accuracy and loss metrics printed during training.



