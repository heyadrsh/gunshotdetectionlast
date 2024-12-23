# Real-time Gunshot Detection System

A deep learning-based system for real-time gunshot detection using audio processing and neural networks.

## Overview

This project implements a real-time gunshot detection system using deep learning techniques. The system processes audio input from a microphone, extracts relevant features, and uses a trained neural network to detect gunshot sounds with high accuracy.

## Features

- Real-time audio processing
- Advanced feature extraction (Mel-spectrogram, MFCC, Similarity Matrix)
- Deep learning model based on ResNet50V2
- High accuracy (99.35% on test set)
- Background noise handling
- Real-time visualization
- Audio clip saving of detected gunshots

## Dataset

The system uses two main datasets:
1. **Gunshot Dataset**: 2,148 samples from 4 different guns
   - Glock 17 9mm (669 samples)
   - S&W .38 Special (503 samples)
   - Remington 870 (379 samples)
   - Ruger AR-556 (597 samples)

2. **UrbanSound8K**: Used for background/non-gunshot sounds

## Technical Architecture

### Components:
1. **Data Loading** (`data_loader.py`)
   - Dataset organization
   - Audio file handling
   - Metadata management

2. **Feature Extraction** (`feature_extraction.py`)
   - Mel-spectrogram generation
   - MFCC extraction
   - Similarity matrix computation

3. **Model Architecture** (`model.py`)
   - ResNet50V2 base
   - Custom layers for gunshot detection
   - Binary classification output

4. **Training Pipeline** (`train.py`)
   - Data preprocessing
   - Model training
   - Validation
   - Checkpointing

5. **Real-time Detection** (`main.py`)
   - Audio capture
   - Real-time processing
   - Detection logic
   - Alert system

## Requirements

```
numpy>=1.19.2
tensorflow>=2.4.0
librosa>=0.8.0
sounddevice>=0.4.1
scipy>=1.6.0
matplotlib>=3.3.2
pandas>=1.2.0
scikit-learn>=0.24.0
PyAudio>=0.2.11
h5py>=3.1.0
tqdm>=4.60.0
```

## Installation

1. Clone the repository:
```bash
git clone https://github.com/heyadrsh/gunshotdetectionlast.git
cd gunshotdetectionlast
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Prepare the dataset:
```bash
python prepare_dataset.py
```

4. Train the model:
```bash
python train.py
```

5. Run real-time detection:
```bash
python main.py
```

## Project Structure

```
project/
├── dataset/
│   ├── gunshots/         # Gunshot audio files
│   ├── urbansound8k/     # Background sounds
│   └── processed/        # Processed features
├── checkpoints/          # Saved models
├── data_loader.py        # Dataset handling
├── feature_extraction.py # Audio feature extraction
├── model.py             # Neural network model
├── train.py             # Training script
├── main.py              # Real-time detection
└── test_detection.py    # Testing utilities
```

## Performance

- Training Accuracy: 99.99%
- Validation Accuracy: 99.57%
- Test Accuracy: 99.35%
- Real-time Processing Delay: ~1.2 seconds

## Future Improvements

1. Multi-gun classification
2. Distance estimation
3. Direction detection
4. Mobile deployment
5. Performance optimization

## Contributing

Feel free to contribute to this project by:
1. Fork the repository
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## Contact

- GitHub: [@heyadrsh](https://github.com/heyadrsh)
- Email: heyadrsh@gmail.com

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

Based on the research paper: "A Multi-Firearm, Multi-Orientation Audio Dataset of Gunshots" by Ruksana Kabealo et al. 