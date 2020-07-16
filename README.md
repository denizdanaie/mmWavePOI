# mmWavePOI

Track, cluster and classify people using the ti mmwave sensor.

This repo is a messy collection of the stuff i did in my thesis. The usefull parts are:

QTGui.py is a capture program for mmwave data.
use `-h` to see the options

labeler/labeler.py is a program to inspect the recorded data, and add labels to them.

RFClassifier.py is a script to try different classification methods based on scikit-learn.

recurrent_networks.ipynb is a jupyter notebook using tensorflow to classify the tracked objects. Implemented is a LSTM and GRU network.
You can use this online in google colab: https://colab.research.google.com/drive/1w-dlOCp_RiF4aoebhJrN33Tra0lLX_z4?usp=sharing

Spread throughout are scripts for inspecting, plotting, and various tools to work with the mmwave data and intermediate formats.

## Package Dependencies

You can find package dependencies in requirements.txt.
To installing these libraries:

```py -m pip install -r requirements.txt```

And specific packages like:

```py -m pip install tensorflow```

(if you have multiple pythons installed you’ll also want the right version, e.g. -3.7-64)
(you could care to isolate via `virtualenv`)

`construct` make the data parsing easier.

`numpy` For the GUI (e.g. QtGUI), recording, labeling, and classification stuff

`msgpack` for serialization of raw / labeled data    (h5py seems abandoned?)

`scikit-learn` used for classification

`joblib` seems used largely to serialize the models

`PySide2`, `PyOpenGL`, `matplotlib` is for GUI plotting stuff

`shiboken2` is required for `PySide2`

`pyserial` Anything that want to talk to the sensor.
   
Experiments like those in RFClassifier also want packages like:
  
`pandas`
  
`seaborn`
  
`statsmodels`

And the neural network code in the notebook:
`tensorflow`
