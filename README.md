# mmWavePOI

Track, cluster and classify people using the ti mmwave sensor.

This repo is a messy collection of the stuff i did in my thesis. The usefull parts are:

`QTGui.py` is a capture program for mmwave data.
use `-h` to see the options. Input files for playback option, from folder `raw/<filename>.bin` can be used. Output files will be of .msgpack format.
```
$ python QTGui.py --h
usage: QTGui.py [-h] [--file FILE] [--playback PLAYBACK] [--clustering]

readout radar sensor

optional arguments:
  -h, --help           show this help message and exit
  --file FILE          filename to store/read
  --playback PLAYBACK  play back file
  --clustering         enable reclustering of pointclouds
```

`labeler.py` is a program to inspect the recorded data, and add labels to them. Input files for playback option, from folder `test31-1/<filename>.msgpack` can be used.

RFClassifier.py is a script to try different classification methods based on scikit-learn.

recurrent_networks.ipynb is a jupyter notebook using tensorflow to classify the tracked objects. Implemented is a LSTM and GRU network.
You can use this online in google colab: https://colab.research.google.com/drive/1w-dlOCp_RiF4aoebhJrN33Tra0lLX_z4?usp=sharing

Spread throughout are scripts for inspecting, plotting, and various tools to work with the mmwave data and intermediate formats.

## Package Dependencies

You can find package dependencies in requirements.txt.
To installing these libraries:

```py -m pip install -r requirements.txt```

For more info about requirements.txt checkout [here](docs/requirements.md)

