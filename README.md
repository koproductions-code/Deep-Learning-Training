# Deep-Learning-Training

## Installation
Clone this repository and cd into it.
```bash
git clone https://github.com/koproductions-code/Deep-Learning-Training
cd Deep-Learning-Training
```

Use pip to install all requirements.

```bash
pip3 install -r requirements.txt
```

Download the dataset from Kaggle:
[https://www.kaggle.com/datasets/shaunthesheep/microsoft-catsvsdogs-dataset?datasetId=550917](https://www.kaggle.com/datasets/shaunthesheep/microsoft-catsvsdogs-dataset?datasetId=550917)

Extract the downloaded file into a new folder "dataset". Your folder structure should now look like this.
```bash
.
├── dataset
│   └── PetImages
│       ├── Cat
│       └── Dog
├── main.py
├── README.md
├── requirements.txt
├── models
└── util
```

Then run this command to rearrange the dataset.
```bash
python3 main.py --create_dataset --dataset [Choose a name, for example, "dataset01"]
```

## Get Started

Train for 10 epochs and save to a specified path.
```bash
python3 main.py --dataset [The name you chose, e.g. "dataset01"] --epochs 10 --train --save [path]
```

Evaluate your existing model.
```bash
python3 main.py --dataset [The name you chose, e.g. "dataset01"] --evaluate --load [path]
```

Use your model to predict an image.
```bash
python3 main.py --dataset [The name you chose, e.g. "dataset01"] --load [model path] --predict [image path]
```

Train an existing model further.
```bash
python3 main.py --dataset [The name you chose, e.g. "dataset01"] --load [old model path] --epochs 10 --train --save [new model path]
```

For more help, look at the "Usage" section or run
```bash
python3 main.py --help
```

## Usage

```bash
usage: main.py [-h] [--create_dataset] [--dataset DATASET] [--load LOAD] [--save SAVE] [--train] [--evaluate] [--predict PREDICT] [--epochs EPOCHS]

Cats and Dogs Deep Learning Classifier

options:
  -h, --help         show this help message and exit
  --create_dataset   Create dataset
  --dataset DATASET  Dataset path
  --load LOAD        Load model weights
  --save SAVE        Save model weights
  --train            Train model
  --evaluate         Evaluate model
  --predict PREDICT  Image path to predict
  --epochs EPOCHS    Define number of epochs
```

## License
MIT
