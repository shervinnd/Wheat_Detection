# Wheat Detection with YOLO 🚜🌾

Welcome to the **Wheat Detection** project! This repository uses the
YOLO11 model to detect wheat heads in agricultural images, leveraging
the GlobalWheat2020 dataset. Perfect for precision agriculture and crop
monitoring! 🌱

## 📖 Overview

This project implements wheat head detection using the Ultralytics YOLO
framework. It includes downloading the GlobalWheat2020 dataset, training
a YOLO11n model, and performing inference on uploaded images. The
results are visualized with bounding boxes around detected wheat heads.
🌾

## 🚀 Features

-   📥 Downloads and organizes the GlobalWheat2020 dataset
-   🛠️ Trains a YOLO11n model for wheat head detection
-   🖼️ Performs inference on uploaded images
-   📊 Visualizes results with bounding boxes using Matplotlib
-   ⚙️ Easy-to-use Python script for end-to-end workflow

## 📋 Requirements

-   Python 3.8+
-   Ultralytics YOLO (`pip install ultralytics`)
-   Matplotlib
-   NumPy
-   Pillow
-   Google Colab (optional for running in the cloud ☁️)

Install dependencies:

``` bash
pip install ultralytics matplotlib numpy pillow
```

## 🛠️ Installation

1.  Clone the repository:

    ``` bash
    git clone https://github.com/your-username/wheat-detection.git
    cd wheat-detection
    ```

2.  Install required packages:

    ``` bash
    pip install -r requirements.txt
    ```

3.  Run the script in a Python environment or Google Colab:

    ``` bash
    python wheat_detection.py
    ```

## 📂 Dataset

The project uses the **GlobalWheat2020** dataset:

-   Images and annotations are downloaded from Zenodo and Ultralytics.
-   The dataset is organized into `images`, `labels`, and `annotations`
    directories.
-   A YAML file (`GlobalWheat2020_subset.yaml`) is created for training
    and validation subsets.

## 🧠 Model Training

The script trains a pre-trained **YOLO11n** model on the GlobalWheat2020
dataset for 5 epochs. Adjust the number of epochs or image size as
needed:

``` python
model.train(data="GlobalWheat2020_subset.yaml", epochs=5, imgsz=640)
```

## 🔍 Inference

Upload an image to perform wheat head detection:

1.  The script prompts for image upload.
2.  Results are displayed with bounding boxes using Matplotlib.

Example:

``` python
results = model("path/to/image.jpg")
for result in results:
    img = result.plot()
    plt.imshow(img)
    plt.show()
```

## 📊 Results

The trained model outputs bounding boxes around wheat heads in images.
Results are saved in the `runs/detect` directory. Example output:

![Wheat Detection Example](sample_output.jpg)\## 🤝 Contributing

Contributions are welcome! 🌟 Feel free to:

-   Open issues for bugs or feature requests
-   Submit pull requests with improvements
-   Add new datasets or enhance the model

## 📜 License

This project is licensed under the MIT License. See the LICENSE file for
details.

## 📬 Contact

For questions or feedback, reach out via GitHub Issues or email at
shervindanesh8282@gmail.com

Happy wheat detecting! 🌾🚀
