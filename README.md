# XRAY-classification-into-normal-and-Viral-Pneumonia

SUMMARY OF THE MODEL BUILT
by PALAK NATH 

STEP 1: IMPORTING THE LIBRARIES
STEP 2: FETCHING DATA and PREPARING THE TRAINING AND TESTING CLASSES
I have taken a dataset of ‘COVID-19 Radiography Database’ with default three folders COVID, VIRAL and NORMAL PNEUMONIA. I took the two folders of Viral and Normal Pneumonia XRAY for the Classification problem given. 
I divided the dataset into two parts: Training, Testing and Validation, I used up around 80% of data for training, remaining 19-20% for testing and kept around 9 pictures for validation prediction.
STEP 3: I used a pie chart to depict the above-mentioned division of data. 
STEP 4: DEFINING THE TRAIN IMAGE GENERATOR: TRAINING DATA PREPROCESSING
I converted images to PIL format so Python can understand using the image generator. Used features such as rescale for data normalization, shear_range for transformation technique to apply on the 2D image for better understanding and zoom_range for setting range for random zoom. 
STEP 5: DEFINING THE TEST IMAGE GENERATOR: TESTING DATA PREPROCESSING: 
I converted images to PIL format so Python can understand using the image generator. Used features such as rescale for data normalization. Didn’t use the other things as I wanted my model to be ready for all kinds of images. 
STEP 6: BUILDING THE MODEL: We will build the CNN model in this step:
-Applied kernel/feature detector on the input image and got value of feature map.
- Decided the number of feature detectors, they can be random. I decided the number of features as 32, then kernel size(feature detector size) here 3x3.
- Defined the input Shape which defines the number of rows and columns the input images take and the number 3 shows we are considering colour images. (in case of black and white images we will choose 1)
While building the CNN model I used Conv2D, max Pooling and Batch Normalization layers. Then Dropout was used to give a random weight to model and to clear out the noisy data present.  Then I used the Flatten function to flatten the layers and finally added my output layer with sigmoid as the activation function as it is used for binary classification. 
STEP 7: COMPILING THE MODEL
As we are to classify only NORMAL OR VIRAL, we use binary cross entropy.
STEP 8: TRAINING THE MODEL: Used 25 Epochs to train my model 
STEP 9: MODEL EVALUATION: Found out Accuracy and plotted the training accuracy vs testing accuracy as well as the training loss vs testing loss. 
STEP 10: MODEL VALIDATION 
Used Prediction function to validate the model. Used confusion matrix which is a clear depiction of evaluation of models. Found the kappa values using the confusion matrix. As I couldn't find the direct code, I read about Kappa from google and calculated it manually using the arithmetic operations of python.






