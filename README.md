# PRODIGY_ML_TASK-04
### Summary of the Code

This Python script is a comprehensive solution for **hand gesture recognition**. It combines a **convolutional neural network (CNN)** for classifying hand gestures with **MediaPipe** for real-time hand detection and tracking.

#### Key Features:
1. **Gesture Dataset Loading and Preprocessing**:
   - The dataset is organized into directories, each representing a specific gesture (e.g., thumbs up, peace sign).
   - Images are loaded, resized to 64x64 pixels, and normalized for input into the CNN.
   - Labels are converted into one-hot encoding for classification.

2. **CNN Model Design**:
   - A sequential model with convolutional, pooling, dropout, and dense layers.
   - Optimized using the Adam optimizer and trained with categorical cross-entropy loss.
   - Designed to classify gestures into predefined categories (e.g., thumbs_up, peace_sign).

3. **Training and Validation**:
   - The dataset is split into training and testing sets using an 80-20 ratio.
   - The model is trained for 10 epochs with a batch size of 32.
   - After training, the model is saved as a `.h5` file for future use.

4. **Real-Time Gesture Recognition**:
   - Utilizes **MediaPipe Hands** to detect and track hand landmarks in real-time video from the webcam.
   - Extracts the bounding box of the hand, crops it, and resizes it to match the model’s input size.
   - Predicts the gesture based on the CNN model and overlays the gesture name and bounding box on the video feed.

5. **User Interaction**:
   - Runs a real-time recognition loop, displaying the video with predicted gestures.
   - Allows the user to exit by pressing 'q'.

#### Practical Applications:
- This code can be used in **human-computer interaction** projects, enabling gesture-based control systems for smart devices, games, or assistive technologies.

#### Potential Enhancements:
- Augmenting the dataset for better model generalization.
- Adding more gestures for broader functionality.
- Optimizing the real-time inference pipeline for performance.

The script is modular, making it easy to expand or adapt for various hand gesture recognition tasks.
