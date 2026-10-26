# Emotion Recognition from Speech

## Project Overview
This project uses speech signal processing and deep learning to recognize emotions from audio recordings. It was developed as a Machine Learning project for the CodeAlpha internship.

## Objectives
- Extract useful audio features using Mel-Frequency Cepstral Coefficients (MFCCs).
- Train deep learning models to classify emotions from speech.
- Evaluate model performance using accuracy, classification reports, and confusion matrices.
- Compare CNN and CNN-LSTM model architectures.

## Dataset
The project uses the RAVDESS speech emotion dataset, containing audio recordings from 24 actors.

The eight emotion classes used in this project are:
- Angry
- Calm
- Disgust
- Fearful
- Happy
- Neutral
- Sad
- Surprised

## Methodology
1. Load and organize the audio recordings.
2. Extract MFCC features using audio signal processing.
3. Convert emotion labels into numerical classes.
4. Split the data into training, validation, and test sets while keeping actors separate between the sets.
5. Train and compare CNN and CNN-LSTM models.
6. Evaluate model predictions using classification reports and confusion matrices.

## Models
The project includes these trained models:
- CNN
- Class-weighted CNN
- CNN-LSTM
- CNN-LSTM with mean pooling

## Results
The current best test accuracy among the evaluated models is:

| Model | Test Accuracy |
|---|---:|
| CNN | 43.67% |
| Class-weighted CNN | 42.33% |
| CNN-LSTM | 36.00% |
| CNN-LSTM with mean pooling | 31.33% |

The CNN achieved the highest test accuracy among these experiments. The results show that emotion recognition remains challenging, and further improvements are needed.

## Project Structure
```text
CodeAlpha_Emotion_Recognition_From_Speech/
â”œâ”€â”€ Audio_Speech_Actors_01-24_16k/
â”œâ”€â”€ data/
â”œâ”€â”€ models/
â”‚   â”œâ”€â”€ emotion_cnn.pth
â”‚   â”œâ”€â”€ emotion_cnn_weighted.pth
â”‚   â”œâ”€â”€ emotion_cnn_lstm.pth
â”‚   â””â”€â”€ emotion_cnn_lstm_meanpool.pth
â”œâ”€â”€ notebooks/
â”œâ”€â”€ results/
â”œâ”€â”€ src/
â”œâ”€â”€ Emotion_Recognition_CNN_recovered.ipynb
â””â”€â”€ README.md
```

## Results and Reports
The `results/` directory contains:
- MFCC feature arrays and emotion labels
- Dataset and processed-file CSV files
- Classification reports
- Confusion matrix images
- Model training histories and test predictions

## Requirements
The project uses Python and libraries including:
- NumPy
- Matplotlib
- scikit-learn
- PyTorch

Some audio-processing components may require additional compatible packages.

## How to Run
1. Open the notebook `Emotion_Recognition_CNN_recovered.ipynb` in Jupyter Notebook or VS Code.
2. Install the required Python packages in a compatible environment.
3. Ensure the RAVDESS dataset is available at the path expected by the notebook.
4. Run the notebook cells in order to process the audio, train the models, and evaluate the results.

The saved models and result files are available in the `models/` and `results/` directories.

## Limitations
The current models have modest test accuracy. Performance may be affected by differences between speakers, overlapping acoustic patterns between emotions, and the limited dataset. The test set should remain separate from model training and model selection.

## Future Improvements
- Improve audio preprocessing and feature normalization.
- Experiment with alternative CNN and recurrent architectures.
- Tune hyperparameters using validation data.
- Apply data augmentation where appropriate.
- Evaluate generalization on additional speech emotion datasets.

## Author
Developed as part of the CodeAlpha Machine Learning Internship.
'@ | Set-Content -Path .\README.md -Encoding utf8

