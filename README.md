# Cat-Dog Image Classifier Web UI

This is a web-based user interface for classifying images as either a cat or a dog. It utilizes a Convolutional Neural Network (CNN) for image classification. Users can upload an image, and the model will predict whether it's a cat or a dog.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Model Training](#model-training)
- [Contributing](#contributing)
- [License](#license)

## Features

- Upload and classify images as either "Cat" or "Dog."
- Real-time predictions with a pre-trained CNN model.
- Simple and intuitive user interface.

## Prerequisites

Before you begin, ensure you have Poetry installed. You can install Poetry by following the instructions [here](https://python-poetry.org/docs/#installation).

## Installation

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/your-username/cat-dog-image-classifier-ui.git
   ```

2. Change to the project directory:

   ```bash
   cd cat-dog-image-classifier-ui
   ```

3. Use Poetry to install the project's dependencies:

   ```bash
   poetry install
   ```

4. Create a virtual environment and install the project's dependencies:

   ```bash
   poetry shell
   ```

## If you want to train the model by yourself, please follow the steps below.
### Data download.

You can download the data from [Here](https://drive.google.com/drive/folders/1AffYjpSNO8PUzPKZ3ZFzXk5sefXIc1X2) or use the script to download the data from Google Drive.

To use the script to download the data from Google Drive:

1. You need to enable the Drive API to use the script. The enabling instructions can be found on [Python Quickstart](https://developers.google.com/drive/api/quickstart/python). The credentials.json file will be needed in the working directory.

2. the Run the script to download the data:

   ```bash
   python /data/download_data.py 1AffYjpSNO8PUzPKZ3ZFzXk5sefXIc1X2
   ```

### Data exploration and preparation.

1. We use jupyter notebook to prepare the data. You can install jupyter notebook by following the instructions [here](https://jupyter.org/install).

2. Run the jupyter notebook:

   ```bash
   jupyter notebook
   ```

3. Open the notebook file `data_preparation.ipynb` and run the cells to prepare the data.

### Model Training

The pre-trained CNN model used in this project was trained on a dataset of cat and dog images. If you wish to retrain the model or fine-tune it for your specific use case, you can follow these steps:

1. Collect a dataset of cat and dog images.

2. Train the model using your dataset and save it.

3. Replace the pre-trained model file in the `models/` directory with your trained model.

4. Update the model loading code in `app.py` to load your custom model.

## Usage

1. Start the web application:

   ```bash
   python app.py
   ```

2. Open your web browser and go to `http://localhost:5000` to access the user interface.

3. Upload an image of a cat or dog using the provided interface.

4. Click the "Classify" button to get the prediction.



## Contributing

Feel free to contribute to this project by opening issues or submitting pull requests. We welcome any improvements or bug fixes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

This README uses Poetry for dependency management and project setup. Be sure to customize it as needed for your specific project and add any additional setup or project-specific details.
