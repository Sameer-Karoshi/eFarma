# eFarma

Identification of plant diseases and providing a remedy is crucial to eliminate farm losses and increase agricultural yield. Every year farmers must bear huge damages due to plant diseases as well as inaccurate choice of crop. The diseases in plants every time cannot be identifies by the naked eye. Also, contacting farm experts is not always feasible. Hence, the use of technology to address the said problems becomes important. Keeping this in mind,developed a system that tells the farmers the type of crop disease from an image and instantly give a solution for the same. Moreover, suitable crop is also suggested based on the soil type and contents, moisture, temperature, humidity, and other environmental conditions. A deep learning algorithm known as Convolution Neural Network (CNN) is used for detection of plant diseases. Suitable crop is recommended using Random Forest Algorithm. An accuracy of 98% is achieved in plant disease detection, while the crops are being recommended with an accuracy of 99%. The system is developed in the form of a website where the farmers can upload an image and the disease type, and its remedy is displayed immediately. Suitable crop is also being advised to the farmers according to the parameters. A platform to buy and sell products online will help the farmers grow in an increasingly digital world. A discussion forum has also been added so that farmers can have their questions answered by the agricultural experts. This project aims to ease the life of the farmers.

## Complete FlowChart of System: 

![alt text](https://github.com/Sameer-Karoshi/eFarma/blob/master/Complete%20FlowChart%20of%20System.PNG)

## A. Plant Leaf Disease Detection

Main objective of this feature is to solve one of the major problems in agriculture, which is to detect disease in plants. Farmers will use this platform to upload images of infected leaves then this model will detect disease and give a proper solution. It will help farmers to tackle these issues in the early stage to improve crop yield and productivity. This section is divided into dataset and CNN model and which will connect our machine learning model with different applications.

**DataSet:**
The dataset consists of 10 different kinds of diseases which are found in tomato leaves such as Bacterial spot, Early blight, Late blight, Leaf mold etc. each one of them contains around 1000 images. Similar datasets have been used for detection of diseases in corn, and potato leaves.

**Convolution Neural Network (CNN):**
Sequential models from Keras are used for classification of leaf diseases. Sequential helps you to build the model layer by layer. Initially, the images have been loaded from the dataset and then resized images to size of 256 x 256. 80% of images are used for training and the remaining 20 % for testing.Also used data augmentation techniques to create new data from existing dataset. This will help to improve the performance of the model. The parameters that were altered to obtain this new data are Rotating Image, Shifting Image Horizontally, Zooming Image up to 20%, Flipping Image Horizontally.

**The flow of classification and detection of leaf diseases is shown in below figure:**

![alt text](https://github.com/Sameer-Karoshi/eFarma/blob/master/Classification%20of%20Leaf%20Diseases.PNG)

There are different activation functions like ReLU, sigmoid, and tanh. The filter results from the previous layer are used before passing it to the next layer. All these layers relate to each other to build a complete convolution neural network. ReLU activation function is used which gives linear output for positive value, otherwise output will be zero.
ReLU Function Equation is: 𝑓(𝑥)=max(0,𝑥)
All these layers are connected with each other to build a complete convolution neural network.

**CNN Visualization Layers:**

![alt text](https://github.com/Sameer-Karoshi/eFarma/blob/master/CNN%20Visualization%20Layers.PNG)

After training model using tomato leaf dataset on GPU provided by Google Colab, an accuracy of 98% was achieved. Training accuracy is achieved from the 80% training data given to the model and validation accuracy is from the rest 20% data. Training data is known to the algorithm, but the validation accuracy is calculated on untrained data. The algorithm already knows the correct answer. It cross-checks the expected and actual output. Hence, training accuracy is always more than validation accuracy. Vertical axis is the accuracy. 1 is the highest value corresponding to 100% accuracy. Number of epochs is depicted on horizontal axis. It was observed that as the number of epochs go on increasing, the training and validation accuracy goes on increasing while the losses go on decreasing.

![alt text](https://github.com/Sameer-Karoshi/eFarma/blob/master/Training%20%26%20Validation%20and%20%20Training%20%26%20Validation%20Loss%20Accuracy.PNG)

## B. Crop Recommendation

Crop Selection has become very important. It is crucial to identify crops that go well with the weather and atmosphere of the land. It is also important to take into consideration the nutrients and chemicals present in the soil before planting the crops. This system takes into consideration all these parameters and suggests the optimal crop . The system takes input of Nitrogen, Phosphorus, Potassium and pH level of the soil along with Temperature, Humidity and Rainfall in the region.

**Dataset:**
The dataset is in the form of a csv file. The dataset consists of 7 parameters namely - Nitrogen level, Phosphorus level, Potassium level, Temperature ,Rainfall in the region ,pH level of soil and humidity. Total 22 crops are included in the database along with the levels of the above-mentioned parameters for each of these crops. In totality 100 data points of each of these crops are included in the dataset. Therefore, there are 2200 different data points in the dataset.
The null values in the dataset are removed. For each of the 100 data-points of each crop the average of each parameter is calculated. So for each crop an optimal level of each parameter is obtained which is most suitable for the respective crop. Supervised Learning algorithms are used for suggestion of the crop. The data is split into 80:20 test train ratio. The model is trained using four supervised learning algorithms such as Logistic Regression, K-Nearest Neighbor, Decision Tree , Random Forest.

It is observed that Random Forest algorithm was the most efficient. The flow of Random Forest algorithm is shown below figure. It is a classifier consisting of many decision trees on different subsets of a dataset and takes a voting (average) to improve the accuracy. Higher accuracy is achieved by a greater number of decision trees and addresses the problem of overfitting.

![alt text](https://github.com/Sameer-Karoshi/eFarma/blob/master/Crop%20Recommendation%20using%20RF.PNG)

## C. Online Marketplace
In the website created a separate section wherein users can buy or sell all the products related to agriculture. MERN Stack is used to develop this platform. Users have to register with their email for buying the products and only verified farmers are able to sell products through this platform. Database used is MongoDB and all the images are stored on the Cloudinary website. 5 product categories and some filters are also applied to ease the product search. PayPal is used as the payment gateway to make the platform fully functional. Currently, the website is locally hosted but using the hosting platforms it can also be made publicly available.

## D. Discussion Forum
This is another feature for farmers. Created one discussion forum for farmers using ReactJS. ReactJS is a library of JavaScript. By using this we can create a UI. Also used a chat engine as a backend for discussion forums. Chat engine is an API. It is an restful API which hosts all our chats and NPM components to help with our Chat UI.

## E. Demo Video of Website

![](https://github.com/Sameer-Karoshi/eFarma/blob/master/Demo.gif)
