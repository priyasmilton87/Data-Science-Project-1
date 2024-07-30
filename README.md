The goal of **Sign Language Detection** was to build and compare different neural network models to identify American Sign Language (ASL) letters from images. The dataset used for this project contains images of hand gestures representing ASL letters (excluding J and Z). The steps and the corresponding code can be summarized as follows:

**Step 1:** **Data Collection and Preprocessing**
Load the Dataset: Loaded training and test datasets from CSV files.
Separate Features and Labels: Separated the pixel values (features) and the corresponding labels (targets).
Normalize the Pixel Values: Scaled pixel values to a range of 0 to 1.
Reshape the Data: Reshaped the data to fit the input shape expected by the models.
Encode the Labels: One-hot encoded the labels to prepare for categorical classification.

**Step 2: Model Development and Comparison**

Three different models were developed:

**1. Simple ANN Architecture:**
Flatten layer to convert 2D images to 1D vectors.
Dense layer with 512 units and ReLU activation.
Dropout layer for regularization.
Dense layer with 256 units and ReLU activation.
Dropout layer.
Output Dense layer with 24 units and softmax activation for classification.
Training: Trained the model using Adam optimizer and categorical cross-entropy loss.

**2. Convolutional Neural Network (CNN)**
Architecture:
Conv2D layer with 32 filters and ReLU activation.
MaxPooling2D layer.
Dropout layer.
Flatten layer.
Dense layer with 512 units and ReLU activation.
Dropout layer.
Output Dense layer with 24 units and softmax activation.
Training: Trained the model similarly to the Simple ANN.

**3. Deep Convolutional Neural Network (Deep CNN)**
Architecture:
Conv2D layer with 32 filters and ReLU activation.
MaxPooling2D layer.
Dropout layer.
Conv2D layer with 64 filters and ReLU activation.
MaxPooling2D layer.
Dropout layer.
Flatten layer.
Dense layer with 512 units and ReLU activation.
Dropout layer.
Output Dense layer with 24 units and softmax activation.
Training: Trained the model similarly to the previous models.

**Step 3: Model Evaluation**

Evaluate Each Model: Evaluated the models on the test set using accuracy, confusion matrix, and classification report.
Comparison of Models:
**Simple ANN Test Accuracy: 0.8063
CNN Test Accuracy: 0.8745
Deep CNN Test Accuracy: 0.9470**

**Step 4: Compare Models**

Plot Training History: Plotted the accuracy and loss during training and validation for each model.
Confusion Matrix and Classification Report: Generated confusion matrices and classification reports to analyze the model performance in detail.
Conclusion
Based on the test accuracies, the Deep Convolutional Neural Network (Deep CNN) performed the best with a test accuracy of 0.9470. 
The CNN performed moderately well with a test accuracy of 0.8745, while the Simple ANN had the lowest performance with a test accuracy of 0.8063. 
The evaluation shows that deeper and more complex models (CNN and Deep CNN) are more effective for image classification tasks like ASL letter recognition.
