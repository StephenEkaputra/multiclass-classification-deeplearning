# multiclass-classification-transferlearning

Dataset are divided into training dataset (2,819 images) and testing dataset (1,040 images). In the training dataset, there are 13 classes. Those are bedroom (136 images), coast (280 images), forest (248 images), highway (180 images), insidecity (228 images), kitchen (130 images), livingroom (209 images), mountain (294 images), office (135 images), opencountry (330 images), street (212 images), suburb (161 images), and tallbuilding (276 images).

Steps:
1.	Set image width and height to 224x224
2.	Set batch size = 32
3.	Data augmentation (rescaling (normalization), flipping, rotating, zooming) and split the dataset into validation dataset (20%) and training dataset (80%)
4.	Set the class mode into categorical because we have 13 classes
5.	Use transfer learning (InceptionV3 GoogleNet)
6.	Use and set the L2 regularizers to 0.005
7.	Use softmax as classifier for 13 classes
8.	Set model check point to save the best weights during the training process by monitoring the loss function
9.	Use ReduceLrOnPlateau to reduce the learning rate value with the minimum learning rate value of 0.001 by the factor of 0.2 if the loss function isn’t improved after 5-epochs
10.	 Use Stochastic Gradient Descent (SGD)
11.	Set steps_per epoch to 70 → Training dataset / batch size
12.	Set validation set to 14 → Validation dataset / batch size
13.	Set the epoch to 70
14.	Train time
15.	Plot the accuracy and loss
16.	Get the weight and choose the best one
17.	Predict Testing dataset
