# ECG-based Patient Classification Model
This project aims to develop a modular architecture model for classifying patients as normal or abnormal using electrocardiogram (ECG) data. The model consists of two branches: a Conv1D branch utilizing residual patterns to enhance convergence and extract relevant patterns from the ECG signals, and an LSTM branch to capture the sequential dependencies within the ECG data. The extracted features from both branches are concatenated and passed through fully connected layers, culminating in a sigmoid layer that outputs the probability of the patient being normal or abnormal.
## Dataset
The model is trained, validated, and tested using a dataset consisting of ECG signals from both normal and abnormal patients. The dataset should be appropriately preprocessed and labeled with the corresponding patient class (normal or abnormal).

## Model Architecture
The model follows a modular architecture, combining Conv1D and LSTM branches to capture relevant features from the ECG signals and make accurate classifications.
### Conv1D Branch
The Conv1D branch utilizes residual connections to expedite convergence and improve the model's ability to learn intricate patterns from the ECG signals. It employs convolutional layers to process the ECG signals, followed by pooling layers for downsampling and reducing the spatial dimensions. The output of the Conv1D branch is a set of extracted features that are vital in distinguishing between normal and abnormal ECG patterns.

### LSTM Branch
The LSTM branch focuses on capturing sequential dependencies present in the ECG signals. By leveraging the recurrent nature of LSTM layers, the branch can comprehend the temporal relationships and long-term dependencies within the data. The LSTM branch processes the ECG signals and outputs a set of learned sequential features that aid in patient classification.
## Concatenation and Fully Connected Layers
The features obtained from the Conv1D and LSTM branches are concatenated and passed through fully connected layers. These layers are responsible for combining the extracted features and learning representations suitable for patient classification. The architecture of the fully connected layers can be adjusted based on the specific requirements of the task.

### Sigmoid Layer
The final layer of the model is a sigmoid layer, which outputs the probability of the patient being normal or abnormal. The sigmoid function squashes the model's output between 0 and 1, providing a probability estimate that can be interpreted as the likelihood of the patient belonging to the abnormal class.'
## Model Evaluation
The model's performance is evaluated using various metrics, including accuracy, precision, recall, and F1-score. Accuracy represents the percentage of correctly classified samples, while precision measures the proportion of correctly classified normal patients out of all patients predicted as normal. Recall, also known as sensitivity, quantifies the proportion of correctly classified normal patients out of all actual normal patients. F1-score provides a balance between precision and recall, considering both metrics to evaluate overall model performance and most of all metrics give most signature if them accuracy is about 100% on most of data (train, valid, test).
## Model Optimization and Deployment
The trained model can be further optimized and converted into a TensorFlow Lite (TFLite) model, enabling efficient deployment on resource-constrained devices like the Raspberry Pi. The TFLite model reduces the model's size and optimizes its execution, making it suitable for real-time patient classification on the Raspberry Pi or similar edge devices.
