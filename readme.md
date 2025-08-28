# 🏆 EPL Logo Detection Project

![EPL Banner](https://raw.githubusercontent.com/RakshakSigdel/Epl_Logo_Detection/main/readme_assets/epl_banner.jpg)

## � Project Overview

This project implements a Convolutional Neural Network (CNN) to detect and classify English Premier League (EPL) club logos. The model can identify logos from all 20 EPL clubs with high accuracy.

## ⚙️ Key Features

- **Deep Learning Model**: Custom CNN architecture for logo classification
- **High Accuracy**: Achieves 97%+ accuracy on test data
- **Easy to Use**: Simple interface for testing new images
- **Visualization**: Displays prediction confidence with visual aids

## �️ Technologies Used

- PyTorch for deep learning model implementation
- torchvision for image transformations and dataset management
- matplotlib for visualization
- PIL (Python Imaging Library) for image processing

## 🗂️ Project Structure

- **logo_detector_train.ipynb**: Notebook containing the training pipeline
- **logo_detector_test.ipynb**: Notebook for testing and inferencing with the trained model
- **epl_logo_cnn.pth**: Saved model weights
- **external_test_images/**: Directory with sample logo images for testing

## 📊 Model Architecture

The model consists of:
1. **Feature Extractor**: 3 convolutional layers with ReLU activation and max pooling
2. **Classifier**: Fully connected layers with dropout for regularization
3. **Output**: 20-class classification (one for each EPL club)

```python
model = nn.Sequential(
    feature_extractor,  # Convolutional layers
    nn.Flatten(),
    nn.Linear(25088, 128),
    nn.ReLU(),
    nn.Dropout(0.5),
    nn.Linear(128, 20)  # 20 EPL clubs
)
```

## 📋 Dataset

The model was trained on the "English Premier League Logo Detection" dataset from Kaggle, containing approximately 20,000 logo images across 20 EPL clubs.

## 📈 Results

- **Training Accuracy**: 98.5%
- **Validation Accuracy**: 97.2%
- **Test Accuracy**: 97.0%

## � Usage

1. Clone the repository:
```bash
git clone https://github.com/RakshakSigdel/Epl_Logo_Detection.git
cd Epl_Logo_Detection
```

2. Install dependencies:
```bash
pip install torch torchvision matplotlib pillow
```

3. Run the test notebook to predict logos:
```bash
jupyter notebook logo_detector_test.ipynb
```

## 📷 Demo

![Prediction Example](https://raw.githubusercontent.com/RakshakSigdel/Epl_Logo_Detection/main/readme_assets/prediction_example.jpg)

## 🔮 Future Improvements

- Implement real-time logo detection from video streams
- Deploy as a web application with a user interface
- Add support for historical club logos

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👥 Contact

Feel free to reach out for any questions or feedback!

- GitHub: [RakshakSigdel](https://github.com/RakshakSigdel)
