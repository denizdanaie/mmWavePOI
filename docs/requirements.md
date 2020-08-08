#requirements.txt
## Package Dependencies

You can find package dependencies in requirements.txt.
To installing these libraries:

```py -m pip install -r requirements.txt```


(if you have multiple pythons installed you’ll also want the right version, e.g. -3.7-64)
(you could care to isolate via `virtualenv`)

### Why you need these packages:
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
