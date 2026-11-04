# Spoken Digit Recognition Using Hidden Markov Models (HMM)

## Overview

This project implements an audio-based spoken digit recognition system using **Hidden Markov Models (HMMs)**.

The system recognizes spoken digits from 0 to 9 using audio recordings from the Free Spoken Digit Dataset (FSDD). It extracts MFCC (Mel-Frequency Cepstral Coefficients) features from speech recordings and trains a separate Gaussian HMM for each digit.

The digit is predicted by comparing the likelihood scores produced by the trained HMMs.

The project also demonstrates the mathematical foundations of HMMs through implementations of the Forward, Backward, and Viterbi algorithms.

## Dataset

**Free Spoken Digit Dataset (FSDD)**

Repository: https://github.com/Jakobovski/free-spoken-digit-dataset

The dataset contains spoken recordings of digits from 0 to 9, recorded by multiple speakers.

## Objectives

- Understand sequential data and probabilistic modeling.
- Extract meaningful acoustic features from speech recordings.
- Implement Hidden Markov Models for speech-pattern recognition.
- Understand hidden states, transition probabilities, and emission probabilities.
- Implement Forward, Backward, and Viterbi algorithms.
- Evaluate the performance of the trained models.

## Algorithms and Techniques

- **MFCC Feature Extraction:** Converts audio recordings into compact acoustic feature sequences.
- **Gaussian Hidden Markov Model:** Models the sequential characteristics of speech using hidden states and Gaussian observation distributions.
- **Forward Algorithm:** Calculates the probability of an observation sequence given an HMM.
- **Backward Algorithm:** Calculates the observation-sequence probability using backward recursion.
- **Viterbi Algorithm:** Finds the most likely sequence of hidden states.

## Methodology

1. Download and explore the Free Spoken Digit Dataset.
2. Load audio recordings and inspect their waveforms.
3. Preprocess audio by trimming silence and standardizing the sampling rate.
4. Extract MFCC features from each recording.
5. Standardize the extracted features.
6. Split the dataset into training and testing sets using a speaker-independent approach.
7. Train a separate Gaussian HMM for each digit (0–9).
8. Calculate the likelihood of test recordings using each trained HMM.
9. Predict the digit using the highest length-normalized log-likelihood.
10. Evaluate the model using classification metrics and a confusion matrix.

## Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Librosa
- hmmlearn
- Scikit-learn
- SoundFile
- Google Colab

## Repository Structure

```text
hmm-speech-recognition/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   └── HMM_Audio_Speech_Recognition.ipynb
│
└── results/
    └── Generated evaluation outputs
```

## How to Run

1. Clone this repository:

   ```bash
   git clone https://github.com/YOUR_USERNAME/hmm-speech-recognition.git
   ```

2. Navigate to the project directory:

   ```bash
   cd hmm-speech-recognition
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Open `notebooks/HMM_Audio_Speech_Recognition.ipynb` in Google Colab or Jupyter Notebook.

5. Execute the notebook cells sequentially.

The notebook downloads the FSDD dataset automatically.

## Limitations

- The project focuses on isolated spoken digit recognition rather than general speech-to-text conversion.
- The dataset is relatively small compared with modern speech datasets.
- Recognition performance may vary depending on the speaker and model configuration.
- Gaussian HMMs with MFCC features provide a classical baseline and may not achieve the performance of modern neural speech-recognition systems.

## Future Improvements

- Perform leave-one-speaker-out cross-validation.
- Experiment with different numbers of hidden states.
- Improve feature extraction using delta and delta-delta MFCCs.
- Compare HMM performance with neural sequence models.
- Develop an interface that accepts audio recordings and predicts spoken digits.

## References

- [Free Spoken Digit Dataset](https://github.com/Jakobovski/free-spoken-digit-dataset)
- [hmmlearn Documentation](https://hmmlearn.readthedocs.io/)
- [Librosa Documentation](https://librosa.org/doc/latest/index.html)
