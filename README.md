# -Hand-Written_Digits---Image-Processing

A project to create a machine learning model that can identify the handwritten digits.Applied CNN.In my first keras sequential i have used a convoulsion 2D,with 32 filters of 3x3, activation filter relu to remove the linearity of the data and maxpooling with pool size 2x2 to reduce the image size and to make it spatially independent.In second pass i am repeating same as pass 1.In pass 3 i am using 64 filters.Flattened the data to make it single dimension.Dropout to make sure no overfitting is there.Final dense of 10 as there are 10 digits to predict(0-9).Final Activation function Softmax as it is a multiclass classification.In order to make the optimizer converge faster and closest to the global minimum of the loss function, i used an annealing method of the learning rate (LR). Its better to have a decreasing learning rate during the training to reach efficiently the global minimum of the loss function. To keep the advantage of the fast computation time with a high LR, i decreased the LR dynamically every X steps (epochs) depending if it is necessary (when accuracy is not improved). With the ReduceLROnPlateau function from Keras.callbacks, i choose to reduce the LR by half if the accuracy is not improved after 3 epochs.In order to avoid overfitting problem, we need to expand artificially our handwritten digit dataset. We can make your existing dataset even larger. The idea is to alter the training data with small transformations to reproduce the variations occuring when someone is writing a digit.
