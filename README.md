# Weed-Detection-using-CNN
This project aims to detect weeds in images using a Convolutional Neural Network (CNN) model. The project combines image data and text data to train a model that can classify images as either "weed" or "non-weed". It provides an end-to-end pipeline, including image preprocessing, text preprocessing, data combination, model training, evaluation, and deployment to a local machine using the a CLI Flask app in python.

# Note 
The dataset in a raw dataset without any preprocessing being done before on it. Due to which the images had to be labelled manually and may be prone to human error. This affected the model accuracy and maybe the predictions too. Due to which the model accuracy was 54% on training as well as validation sets. After fine-tuning and hyperparameter tuning and some more data preprocessing the accuracy may subjected to increase.

# Dataset
The dataset used in this project consists of images and corresponding labels indicating whether the image contains a weed or not. The images are stored in the train_images directory, and the labels are provided in the labels.csv file.

# Preprocessing
Image Preprocessing : 
The image preprocessing includes resizing the images to a fixed size (e.g., 224x224 pixels) and converting them to an array format suitable for feeding into the CNN model. The cv2 library is used to read and preprocess the images.
The images are resized to a fixed size, typically to a square shape, such as 224x224 pixels. Resizing the images to a consistent size is important to ensure that all images have the same dimensions, as CNN models require inputs of fixed dimensions.
The cv2 (OpenCV) library is utilized for reading and preprocessing the images. OpenCV provides a wide range of image processing functions that can be used to manipulate and transform images. In this case, it is used to read the images from the file system and perform resizing.By performing these preprocessing steps, the images are prepared in a standardized format suitable for input into the CNN model. This ensures that the model receives consistent input data and allows it to learn meaningful patterns and features for weed detection.


# Model Architecture
The CNN model architecture used for this project consists of several convolutional layers, pooling layers, and fully connected layers. The architecture is designed to learn discriminative features from the images and make predictions based on those features. The model is implemented using the Keras API provided by TensorFlow. The model architecture determines how the layers and operations are organized and connected, allowing the model to learn and extract meaningful features from the input images. The model is compiled using the categorical cross-entropy loss function, which is suitable for multi-class classification problems. The Adam optimizer is used for optimization, and the accuracy metric is used to evaluate the performance of the model during training.

Feel free to modify and experiment with the model architecture to suit your specific needs. You can add more Convolutional layers, adjust the number of filters or kernel sizes, include regularization techniques like dropout or batch normalization, or explore different activation functions to enhance the model's performance.

# Model Training
The model is trained on the preprocessed image data and corresponding labels. The training process involves feeding the data into the model, optimizing the model parameters using an appropriate optimizer (e.g., Adam), and minimizing the categorical cross-entropy loss. The model is trained for a specified number of epochs to improve its performance.

# Evaluation
The trained model's performance is evaluated using various metrics such as accuracy, precision, and F1 score. The evaluation is performed on a separate testing dataset that was split from the original dataset during the data preparation phase.

# Deployment
The trained model can be deployed locally to make predictions on new, unseen images. The deployment involves loading the trained model, preprocessing the input image, passing it through the model, and obtaining the predictions. Deploying a machine learning model using Flask allows you to create a web application that exposes an API endpoint to make predictions based on the trained model. 

The Flask app will start running, and you can send POST requests to http://localhost:5000/predict with an image file to get predictions.

# Usage
To use this project, follow these steps:

Prepare your dataset by organizing the images in the train_images directory and providing the corresponding labels in the labels.csv file.
Run the preprocessing steps to preprocess the images and text data.
Combine the preprocessed data.
Train the CNN model using the combined data.
Evaluate the trained model's performance using the provided metrics.
Deploy the trained model to make predictions on new images.
Please refer to the project's code and comments within each file for more detailed instructions and configurations.

# Dependencies
This project requires the following dependencies:

Python (>= 3.6)
numpy
pandas
scikit-learn
opencv-python
TensorFlow (>= 2.0)
To install the dependencies, you can use the following command:
pip install -r requirements.txt


# Conclusion
This project provides a pipeline for weed detection using a CNN model. By leveraging both image and text data, the model can accurately classify images as either "weed" or "non-weed". The provided documentation and code should assist you in replicating the project's results, as well as extending it to suit your specific needs.

Feel free to contribute to this project by opening issues, suggesting improvements, or submitting pull requests. Happy coding!
