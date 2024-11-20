# Image Segmentation using K-Means Clustering

This repository contains a Python implementation of image segmentation using K-means clustering. The code demonstrates how to segment images by clustering pixels based on their color values.

## Features

- Image loading and preprocessing using PyTorch and PIL
- K-means clustering implementation using scikit-learn
- Visualization of segmentation results with different cluster counts (K=3,4,5,6)
- Support for batch processing multiple images
- Integration with Google Colab and Google Drive

## Requirements

```
torch
torchvision
Pillow
scikit-learn
matplotlib
numpy
```

## Installation

```bash
pip install torch torchvision Pillow scikit-learn matplotlib numpy
```

## Usage

1. Mount Google Drive (if using Google Colab):
```python
from google.colab import drive
drive.mount('/content/drive')
```

2. Load and segment a single image:
```python
image_tensor = load_preprocess_image('path/to/your/image.jpeg')
apply_k_means(image_tensor)
```

3. Process multiple images:
```python
image_paths = [
    'path/to/image1.jpeg',
    'path/to/image2.jpeg',
    'path/to/image3.jpeg'
]

for image_path in image_paths:
    image_tensor = load_preprocess_image(image_path)
    apply_k_means(image_tensor)
```

## Functions

- `load_preprocess_image(image_path)`: Loads and preprocesses an image into a PyTorch tensor
- `apply_k_means(image_tensor, k_values=[3,4,5,6])`: Applies K-means clustering and visualizes results

## Output

The script generates visualizations showing the original image segmented with different numbers of clusters (K values). Each visualization displays how the image looks when divided into K different color segments.

## Contributing

Feel free to open issues or submit pull requests for improvements.

## License

[MIT License](LICENSE)
