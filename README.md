# 🎵 Music Genre Classification with GTZAN Dataset

This deep learning project classifies music genres using audio data from the **GTZAN dataset**. The workflow includes audio preprocessing, spectrogram-based feature extraction, and genre prediction using a **1D Convolutional Neural Network (CNN)**.

## 🎼 Dataset

The [GTZAN Genre Collection](https://www.dropbox.com/scl/fi/logv7hsjc1t3daaysuhyh/genres.tar.gz?rlkey=vcu3jvliyletkjwxz8bv8jm7c&e=2&dl=0) consists of:
- 1000 audio tracks (each 30 seconds long)
- 10 genres: Blues, Classical, Country, Disco, Hip-Hop, Jazz, Metal, Pop, Reggae, Rock

## ⚙️ Methodology

1. **Audio Extraction**  
   - Loaded `.au` files from the GTZAN dataset.

2. Feature Extraction  
   - Converted each audio signal into a **spectrogram image**.
   - Extracted 1D feature vectors from spectrograms for model input.

3. Model Architecture
   - Built a 1D CNN to classify genres based on extracted features.
   - Trained the model on preprocessed data and evaluated its performance.

## 🧠 Model Summary

- Input: 1D feature vectors derived from spectrograms  
- Layers: Conv1D → ReLU → MaxPooling → Dense → Softmax  
- Output: 10 genre classes



## 🧪 Results

- Achieved a test accuracy of 52.6%
- Showed good performance on distinguishing Classic and Country genres

- Classification Report:
                
      .        precision    recall  f1-score   support
      blues        0.44      0.40      0.42        20  
      classical    0.91      1.00      0.95        20
      country      0.37      0.90      0.52        20
       disco       0.42      0.70      0.53        20
      hiphop       1.00      0.10      0.18        20
        jazz       0.75      0.60      0.67        20
       metal       1.00      0.20      0.33        20
         pop       0.85      0.55      0.67        20
      reggae       0.62      0.50      0.56        20
        rock       0.11      0.17      0.13        12

      accuracy                           0.53       192
      macro avg       0.65      0.51      0.50       192
      weighted avg       0.67      0.53      0.51       192


## Comments: The Model showed over-fitting over longer no. of epochs but gave lesser accuracy on lower no. of epochs
## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/gtzan-music-genre-classification.git
   cd gtzan-music-genre-classification

