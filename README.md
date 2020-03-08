# HW_digi_rec

This repository contains a GUI application that detects the numbers drawn in the canvas region

## Getting Started

Follow these steps to deploy a copy of this web application on your system

### Prerequisties

You will need the following tools to deploy this application

Python along with an environment for running .ipynb files is required along with the following python libraries
```
tensorflow
keras
```


### Installing

Execute the Following Commands in the terminal/ command-prompt of your system

```
git clone https://github.com/vini7148/HW_digi_rec.git
cd HW_digi_rec
```

### Running the model

After acquiring all the required pyhton libraries and an envitronment for executing .ipynb files along with this model. Open the "Digit_recognition.ipynb" file

### Deploying this model 

This model is deployed using the python's built-in library Tkinter

## ScreenShot

![Recognizer_1](https://github.com/vini7148/HW_digi_rec/blob/master/ss/1.png)


![Recognizer_2](https://github.com/vini7148/HW_digi_rec/blob/master/ss/2.png)


![Recognizer_3](https://github.com/vini7148/HW_digi_rec/blob/master/ss/3.png)

## Viewing the Application

Just open 'launch.vbs', it should automatically create a new windows for the GUI

## Description of the keras.sequential model

The activation function used is
```
activation = relu
```
The optimizer used is
```
optimizer = keras.optimizers.Adadelta()
```
The summary of the model is 
```
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d_1 (Conv2D)            (None, 26, 26, 32)        320       
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 24, 24, 64)        18496     
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 12, 12, 64)        0         
_________________________________________________________________
dropout_1 (Dropout)          (None, 12, 12, 64)        0         
_________________________________________________________________
flatten_1 (Flatten)          (None, 9216)              0         
_________________________________________________________________
dense_1 (Dense)              (None, 256)               2359552   
_________________________________________________________________
dropout_2 (Dropout)          (None, 256)               0         
_________________________________________________________________
dense_2 (Dense)              (None, 10)                2570      
=================================================================
Total params: 2,380,938
Trainable params: 2,380,938
Non-trainable params: 0
_________________________________________________________________
```
### Training of the model

This model was trained for 10 epochs

## Outcome of this model

For the last epoch the loss, mean absolute error, etc. is
```
Epoch 10/10
60000/60000 [==============================] - 5s 84us/step - loss: 0.0201 - acc: 0.9937 - val_loss: 0.0239 - val_acc: 0.9921
```

The accuracy for the test result is as follows
```
Test loss: 0.02389836816415991
Test accuracy: 0.9921
```

## Built With

* [Python 3](https://www.python.org/ftp/python/3.8.0/python-3.8.0.exe)
* [Anaconda](https://www.anaconda.com/distribution/#download-section)
* Jupyter notebook```conda install -c conda-forge jupyterlab```

Note if you have not install Anaconda, you can still install Jupyter Notebook by ```pip install jupyterlab```


## Authors

* **Vinayak Goswami** - *Initial work* - [vini7148](https://github.com/vini7148)