This directory contains helper functions.

**frameParser.py**: parses sensor data

**util.py**: mainly startSensor()   (itself mainly ‘open serial port, send config text file’)

**POI.py**:
    
    POI class: (used by QtGUI, others)

    Contains clusters over time (identity assigned by the clustering in the sensor)

    POITracker class:
    decides when to add new POI class, and whether to save ones that are gone

    Predictor class: (not finished?, not actively used?)

    loads scaler.joblib     (sklearn.preprocessing.StandardScaler instance)
    
    loads randomForrest.joblib (sklearn.tree.DecisionTreeClassifier instance)
**classifier.py** ?
