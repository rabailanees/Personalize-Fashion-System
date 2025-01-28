# Personalized Fashion System

## Overview

The **Personalized Fashion System** is designed to provide personalized fashion recommendations based on user preferences. It uses **transfer learning with ResNet-50** and the **Annoy** optimized K-Nearest Neighbors (K-NN) algorithm to deliver accurate style suggestions. The system leverages a dataset of over **45,000 fashion images** to extract features and recommends the top 5 closest matches by performing a similarity search.

## Features
- **ResNet-50 Transfer Learning**: Utilizes a pre-trained ResNet-50 model to extract high-level features from fashion images.
- **Annoy K-NN Algorithm**: Implements Annoy's optimized K-NN algorithm for efficient similarity search and quick retrieval of fashion recommendations.
- **Personalized Recommendations**: Provides the top 5 closest matches to a given fashion image, tailored to the user’s style.

## How it Works
1. **Image Feature Extraction**: The system extracts features from a large set of fashion images using the ResNet-50 model, which has been pre-trained on ImageNet data.
2. **Similarity Search**: The extracted features are indexed using Annoy, enabling fast and efficient similarity searches.
3. **Recommendation Generation**: Given a fashion image, the system retrieves the top 5 closest matches from the index, offering personalized style suggestions.

## Requirements

- Python 3.x
- `tensorflow` (for ResNet-50 model)
- `annoy` (for K-NN algorithm)
- `numpy` (for numerical operations)
- `matplotlib` (for visualizations)
- `Pillow` (for image processing)
- `scikit-learn` (optional, for further analysis)

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/Personalized-Fashion-System.git
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Preprocess Images**: Organize your fashion dataset into a folder structure with each category of images stored in its respective folder.
2. **Feature Extraction**: Use the provided script to extract features from the fashion images:
    ```bash
    python extract_features.py --dataset_path <path_to_dataset>
    ```
3. **Build Index**: Once features are extracted, build the Annoy index:
    ```bash
    python build_index.py --feature_file <path_to_feature_file>
    ```
4. **Generate Recommendations**: To get personalized fashion recommendations, run the recommendation script:
    ```bash
    python recommend.py --query_image <path_to_query_image>
    ```

## Example

```bash
python recommend.py --query_image /path/to/your/fashion/image.jpg
```

This will return the top 5 closest fashion images from the dataset, offering personalized recommendations based on visual similarity.

## Contributing

Feel free to fork the repository, open issues, and submit pull requests. Contributions are always welcome!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
