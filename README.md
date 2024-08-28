# Compact Hybrid Neural Network for Pathological Gait Detectionv
This repository contains the code and resources for the paper **"Compact Hybrid Neural Network for Pathological Gait Detection Using Skeleton and Pressure Data"** by Lorenzo Barbiero and Francesco Zane.

## Overview

This project focuses on developing a compact hybrid neural network for detecting pathological gait using multimodal data from non-wearable sensors. The proposed model efficiently combines 3D skeleton data collected from a Microsoft Azure Kinect with foot pressure data from the GW1100 Pressure Plate. The resulting hybrid CNN-based model is lightweight, with only 750k parameters (2.75 MB), achieving a global validation accuracy of 86.9% and class-specific accuracy greater than 93%.

### Key Contributions

- **Hybrid Architecture**: A novel hybrid learning framework that integrates skeletal and foot pressure data for accurate gait classification.
- **Efficiency**: A lightweight model with fewer than 750k parameters, suitable for real-world applications with minimal resource requirements.
- **Accuracy**: Achieves a global validation accuracy of 86.9%, with class-specific accuracies exceeding 93%.
  
## Gait Types Classified

The model classifies six different types of gait:

1. **Normal gait**
2. **Antalgic gait** (pain-induced, limping)
3. **Stiff-legged gait** (stiff knee or hip)
4. **Lurching gait** (gluteus maximus weakness)
5. **Steppage gait** (foot drop)
6. **Trendelenburg gait** (gluteus medius weakness)

## Methodology

### Data Collection

- **Skeleton Data**: Captured using Microsoft Azure Kinect, which tracks 32 joints of the human body in 3D space.
- **Pressure Data**: Collected using the GW1100 pressure plate, producing 128x48 pixel images representing foot pressure during walking.

### Data Processing

- **Preprocessing**: Includes data normalization, noise removal, joint selection, and augmentation techniques like random flipping and cropping.
- **Learning Framework**:
  - **Skeleton Encoder**: Explores RNN, CNN, and CNN-Inception architectures.
  - **Pressure Encoder**: Utilizes CNN-based architecture for feature extraction.
  - **Fusion Model**: Combines skeleton and pressure features for final classification.
  - **Training**: Three different training approaches (0-step, 1-step, 3-step) are explored.

### Results

- **Single-Mode Classification**: Skeleton data outperforms pressure data with an accuracy of 84.8% versus 43.7%.
- **Multi-Mode Classification**: The best hybrid model achieves a validation accuracy of 86.9% and a test accuracy of 96.7% when using the 3-step training method.

## Conclusion

This research demonstrates the potential for implementing lightweight, efficient gait recognition systems in everyday devices, potentially enabling early detection and intervention for gait-related health issues.

## Authors

- **Lorenzo Barbiero**
- **Francesco Zane**

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
