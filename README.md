# Hand Writing Recognizer - Multi Layer Perceptron Neural Network
<p>
This is a multi-layer perceptron neural network written using Jupyter Notebooks to read handwritten characters as pictures and convert them to a digital copy of the same content. The EMNIST dataset was used to train the neural network.<br />
<br /> <b>88% accuracy was achieved in predicting the hand written text</b>
<br />
<br />
<b>Some important links:</b>
<br />
<br />
1. EMNIST dataset which was the input to train the data:
<br />
https://www.nist.gov/node/1298471/emnist-dataset
<br />
2. Python package to read and manipulate the EMNIST data set:
<br />
https://pypi.org/project/emnist/
<br />
3. The hand written images that were used as input post training:
<br />
https://github.com/crash-course-ai/lab1-neural-networks/tree/master/letters
<br />
4. Output files:
<br />
&nbsp;&nbsp;&nbsp;&nbsp;4.a. Jupyter Notebook file:<br />
&nbsp;&nbsp;&nbsp;&nbsp;https://github.com/tebbythomas/Hand_Writing_Recognizer/blob/master/Hand_Writing_Recognizer.ipynb
<br />
&nbsp;&nbsp;&nbsp;&nbsp;4.b. Jupyter Notebook file as HTML:<br />
&nbsp;&nbsp;&nbsp;&nbsp;https://github.com/tebbythomas/Hand_Writing_Recognizer/blob/master/Hand_Writing_Recognizer.html
<br />
<br />
<b>The major steps involved are:</b>
<br />
<br />
1. <b>Retrieving training data:</b>
<br />
The EMNIST dataset() of publicly available handwritten characters and EMNIST Python packages (https://github.com/sorki/python-mnist) required to read and understand the data were downloaded. Each image is a 28 by 28 pixel image.
<br />
&nbsp;&nbsp;&nbsp;&nbsp;1.1. Dividing the data into training and testing
<br />
&nbsp;&nbsp;&nbsp;&nbsp;The first 60,000 hand written images were used as training data and next 10,000 hand written images were used as testing data
<br />
&nbsp;&nbsp;&nbsp;&nbsp;1.2. Drawing a test training data symbol using matplotlib to actually see if the EMNIST data was read.
<br />
<br />
2. <b>Building the multi-layer perceptron (MLP) neural network</b>
<br />
An MLP Classifier was built using Sci-kit learn modules to build a neural network with 1 input layer containing 784 neurons (because each image is a 28pixel by 28 pixel image to a total of 28*28=784 pixels),  1 hidden layer containing 50 neurons and 20 iterations
<br />
<br />
3. <b>Training the MLP neural network </b>
<br />
&nbsp;&nbsp;&nbsp;&nbsp;3.1. The neural network was fit with the training data - 88% accuracy was achieved for the training data and 84% for the testing data
<br />
&nbsp;&nbsp;&nbsp;&nbsp;3.2. Errors in predicting the training set were visualized using a confusion matrix
<br />
&nbsp;&nbsp;&nbsp;&nbsp;3.3. MLP was improved to include 5 hidden layers of 100 neurons each and 50 iterations - <b>88% accuracy was achieved for the training data and 84% for the testing data</b>
<br />
<br />
4. <b>Reading, pre-processing and predicting the hand written characters</b>
<br />
&nbsp;&nbsp;&nbsp;&nbsp;4.1. Input hand written letters were retrieved from here: https://github.com/crash-course-ai/lab1-neural-networks/tree/master/letters
<br />
&nbsp;&nbsp;&nbsp;&nbsp;4.2. Symbols were read using open cv
<br />
&nbsp;&nbsp;&nbsp;&nbsp;4.3. Pre-processing was done to convert the images into the right size of 28 by 28 pixels.
    <br />
&nbsp;&nbsp;&nbsp;&nbsp;4.4. Checked for blank images in the input pictures
    <br />
&nbsp;&nbsp;&nbsp;&nbsp;4.5. Some preprocessing was done to make the input data more similar to the EMNIST data -  because the neural network was trained using that data.
<br /> This involved applying a Gaussian Blur and centering the image to make it similar to the EMNIST images.
<br />
&nbsp;&nbsp;&nbsp;&nbsp;4.6. <b>Predicted the input hand written text with 88% accuracy</b>
<br />
<br />
<b>Screenshots:</b>
<br />
1. <b>Reading EMNIST Input Data</b>:
<br />
<img src="https://github.com/tebbythomas/Hand_Writing_Recognizer/blob/master/Screenshots/EMNIST_Input_Hand_Writing_Proj.png" hspace="20">
<br />
<br />
2. <b>Training the algorithm using the EMNIST Data</b>:
<br />
<img src="https://github.com/tebbythomas/Hand_Writing_Recognizer/blob/master/Screenshots/Training_MLP-Hand_Writing_Proj.png" hspace="20">
<br />
<br />
3. <b>Result after Learning</b>:
<br />
<img src="https://github.com/tebbythomas/Hand_Writing_Recognizer/blob/master/Screenshots/Training_Result-MLP-Hand_Writing_Proj.png" hspace="20">
<br />
<br />
4. <b>Input Letters</b>:
<br />
<img src="https://github.com/tebbythomas/Hand_Writing_Recognizer/blob/master/Screenshots/Input-Letters-Hand_Writing_Proj.png" hspace="20">
<br />
<br />
5. <b>Applying a Gaussian Blur to the input letters to better match the EMNIST input that the algorithm was trained on</b>:
<br />
<img src="https://github.com/tebbythomas/Hand_Writing_Recognizer/blob/master/Screenshots/Applying_Gaussian_Blur-Input-Hand_Writing_Proj.png" hspace="20">
<br />
<br />
6. <b>Results after reading the input and applying the neural net</b>:
<br />
<img src="https://github.com/tebbythomas/Hand_Writing_Recognizer/blob/master/Screenshots/Output-Characters_Recognized.png" hspace="20">
<br />
<br />
