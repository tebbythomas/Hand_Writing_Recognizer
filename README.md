# Hand Writing Recognizer Neural Network
<p>
This is a multi-layer perceptron neural network written using Jupyter Notebooks to read handwritten characters as pictures and convert them to a digital copy of the same content. <br />
<br /> <b>88% accuracy was achieved in predicting the hand written text</b>
<br />
The major steps involved are:
<br />
1. <b>Retrieving training data:</b>
<br />
The EMNIST database (https://github.com/sorki/python-mnist) of publicly available handwritten characters  and EMNIST libraries required to read and understand the data were downloaded. Each image is a 28 by 28 pixel image.
<br />
    1.1. Dividing the data into training and testing
    <br />
    The first 60,000 hand written images were used as training data and next 10,000 hand written images were used as testing data
    1.2. Drawing a test training data symbol using matplotlib to actually see if the EMNIST data was read.
    <br />
<br />
2. <b>Building the multi-layer perceptron (MLP) neural network</b>
<br />
An MLP Classifier was built using Sci-kit learn modules to build a neural network with 1 input layer containing 784 neurons (because each image is a 28pixel by 28 pixel image to a total of 28*28=784 pixels),  1 hidden layer containing 50 neurons and 20 iterations
<br />
3. <b>Training the MLP neural network </b>
<br />
    3.1. The neural network was fit with the training data - 88% accuracy was achieved for the training data and 84% for the testing data
    <br />
    3.2. Errors in predicting the training set were visualized using a confusion matrix
    <br />
    3.3. MLP was improved to include 5 hidden layers of 100 neurons each and 50 iterations - <b>88% accuracy was achieved for the training data and 84% for the testing data</b>
    <br />
<br />
4. <b>Reading, pre-processing and predicting the hand written characters</b>
<br />
    4.1. Input hand written letters were retrieved from here: https://github.com/crash-course-ai/lab1-neural-networks/tree/master/letters
    <br />
    4.2. Symbols were read using open cv
    <br />
    4.3. Pre-processing was done to convert the images into the right size of 28 by 28 pixels.
    <br />
    4.4. Checked for blank images in the input pictures
    <br />
    4.5. Some preprocessing was done to make the input data more similar to the EMNIST data -  because the neural network was trained using that data.
    <br /> This involved applying a Gaussian Blur and centering the image to make it similar to the EMNIST images.
    <br />
    4.6. <b>Predicted the input hand written text with 88% accuracy</b>
