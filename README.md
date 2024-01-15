# Mobile Phone Defect Segmentation using UNet

This project implements a deep learning model to identify defects on mobile phone screens, such as cracks, spots, or oil stains. The goal is to automate visual inspection to catch defects early in the manufacturing process.

## Data Source

The dataset used to train the model is available at [Dataset Ninja](https://datasetninja.com/mobile-phone-defect-segmentation). The dataset contains 1200 images of mobile screens with three types of defects: oil, scratches, and stains. Each image has a corresponding mask that highlights the defect location.

The dataset is split into training and validation sets, with 960 images in the training set and 240 images in the validation set.

## Model Architecture

The U-Net model architecture consists of an encoder-decoder network with skip connections. The encoder downsamples the input image, extracting high-level features, while the decoder then upsamples these features to produce a segmentation mask. The skip connections help in precise localization of defects by combining low-level and high-level features.

The architecture includes:
- Encoder with convolutional layers and max-pooling layers
- Bottleneck layer
- Decoder with transpose convolutional layers and skip connections

## Results

After training the U-Net model, it achieved 99% training accuracy and 99.6% validation accuracy, indicating its ability to accurately segment defects.

## Requirements

To run the code in this repository, you will need the following packages:

- `os`
- `matplotlib`
- `pillow`
- `numpy`
- `pandas`
- `sklearn`
- `random`
- `keras`

These can be installed via pip:

```python
pip install os matplotlib pillow numpy pandas sklearn random keras
```

## Contributing

Contributions, issues, and feature requests are welcome.

## License

See `LICENSE` for more information.
