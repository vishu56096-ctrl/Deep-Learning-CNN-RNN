# Deep Learning: CNN and RNN

Two PyTorch notebooks: image classification on CIFAR-10 (CNN) and sentiment analysis on IMDB movie reviews (RNN).

## Datasets

- **CIFAR-10** — downloaded automatically by `torchvision` into `data/cnn/`.
- **IMDB Dataset.csv** — download instructions are in [`data/README.md`](data/README.md).

## Models

- **CNN:** three convolutional blocks (32, 64, 128 channels), each with ReLU and max pooling, followed by a fully connected classifier (256 hidden units, 10 classes). Trained with Adam and cross-entropy loss for 10 epochs, batch size 64.
- **RNN:** a one-layer vanilla RNN with 64 hidden units. Its final time-step output passes through a fully connected binary classifier.

## Run

Install the dependencies with `pip install -r requirements.txt`, then open the notebooks in VS Code or Jupyter and run the cells in order. Prepare `IMDB Dataset.csv` as described in [`data/README.md`](data/README.md).

## Results

These values are from the notebooks' saved outputs (single run, no hyperparameter tuning):

| Model | Dataset | Test accuracy | Training loss (epoch 1 → 10) |
|---|---|---|---|
| CNN | CIFAR-10 | **74.75%** | 0.136 → 0.064 |
| RNN | IMDB Dataset | **85.39%** | 0.4046 → 0.2054 |

## Project structure

```text
deep-learning-cnn-rnn/
├── README.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   ├── 01_cnn_cifar10_image_classification.ipynb
│   └── 02_rnn_imdb_sentiment_analysis.ipynb
└── data/
    ├── README.md
    ├── cnn/    # downloaded CIFAR-10 files (not tracked)
    └── rnn/    # IMDB Dataset.csv (not tracked)
```

## Author

Vishal Kumar — [GitHub](https://github.com/vishu56096-ctrl)