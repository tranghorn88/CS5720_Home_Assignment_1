# CS5720_Home_Assignment_1

## Student Information:
Name: Trang Horn
ID: 700683454

## Task 1: Tensor Manipulation & Reshaping - Tensor Reshaping & Operations
### Description: 
- A random tensor of shape `(4, 6)` was created using TensorFlow
- Its shape and rank were determined and printed out.
- The tensor was reshaped to `(2, 3, 4)` and then transposed to `(3, 2, 4)`
- A smaller tensor of shape `(1, 4)` was created, then broadcast and added to the transposed tensor.

### Broadcasting Explanation
Broadcasting allow TensorFlow to automatically expand dimensions so that tensor with different shapes can still be added together without explicitly replicating data. In our assignment, TensorFlow automatically expands the dimensions of the smaller tensor `(1, 4)` to match the shape `(3, 2, 4)` during the element-wise addition.

## Task 2:  Loss Functions & Hyperparameter Tuning - Implement and Compare Loss Functions
### Description:
- Defined ground true value (`y_true`) and two predicted values (`y_pred1` and `y_pred2`).
- Computed Mean Squared Error (MSE) and Categorical Cross-Entropy (CCE) losses.
- Compared how small changes in predictions affected the loss values
- A bar chart was plotted to compare the four different loss values (MSE1, MSE2, CCE1, CCE2)
   
## Task 3: Train a Model with Different Optimizers - Train MNIST Model with Adam & SGD
### Description:
- Loaded and normalized the MNIST dataset
- Reshape 28x28 images to 784-length vectors and back to image format inside the model
- Created CNN architecture using `Conv2D`, `MaxPooling2D`, `Flatten`, and `Dense`
- Trained two models: one with the Adam optimizer and one with the SGD optimizer
- Plotted and compared both training and validation accuracy over 5 epochs.
### Observation:
Adam typically converged faster. It yielded higher training accuracy and validation accuracy than SGD within the same number of epochs. Note: convergence refers to how quickly a model's loss decreases and accuracy increases as it learns from the data over time (epochs). Each epoch represents one full pass through the training dataset. Adam typically reaches high accuracy or low loss more quickly. 

## Task 4: Train a Neural Network and Log to TensorBoard
### Description:
-Loaded and preprocessed the MNIST dataset.
- Built a CNN using `Conv2D`, `MaxPooling2D`, `Flatten`, and `Dense`
- Trained the model for 5 epochs and logged metrics (accuracy, loss) using TensorBoard.
- Visualized training and validation performance
- Use TensorBoard to interpret results and answer analysis questions.
### Questions to Answer:
- What patterns do you observe in the training and validation accuracy curves? Both training and validation accuracy curves increase over the 5 epochs. Specifically, the training accuracy increased from 95.6% to 98.5%, and the validation accuracy increased steadily from 98.5% to 99.1%. This CNN model is generating well to unseen data.

- How can you use TensorBoard to detect overfitting? TensorBoard helps detect overfitting by comparing training vs. validation loss and accuracy. If it is observed that training accuracy keeps increasing but validation accuracy stops improving or starts dropping, at the same time, validation loss increases while training loss keeps decreasing, then it is overfitting.

- What happens when you increase the number of epochs? When you increase the number of epochs:
 Initially, both training and validation accuracy will improve. Then, after a point, training accuracy may continue to rise, but validation accuracy might plateau or drop. For example, when I increased the number of epochs from 5 to 10, initially, the training accuracy improved. Validation accuracy also improved, but then began to slightly decrease after epoch 8. TensorBoard visualization helped identify this trend. 



  


