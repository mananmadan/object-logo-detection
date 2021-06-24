## Object and Logo Detection

### Installation and Running
- See in Colab Notebook
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1O84ALermB0Jh6MFe1mGAfFc1aP03eOae?usp=sharing)
- [Open in Jupyter](https://github.com/mananmadan/object-logo-detection/blob/master/Vision_Detection_System_(Video_%2B_DeepLogo)_Final.ipynb)

### File Structure
- Imp Files Modified in Yolov4 + deepsort
    - [object_tracker.py](https://github.com/mananmadan/yolov4-deepsort/blob/3d4ef1627a828f894b74b754df9a5db3ada3584a/object_tracker.py) : Implements yolov4 + deepsort and stores the segmented image of each object in a folder
    - [object_tracker-logo.py](https://github.com/mananmadan/yolov4-deepsort/blob/3d4ef1627a828f894b74b754df9a5db3ada3584a/object_tracker-logo.py) : Implements yolov4 + deepsort + DeepLogo for realtime detection according to the algo A as given in algo.md files
        - Outputs a Dict contains object , their ids and detected logo
    - [object_tracker_logonew.py](https://github.com/mananmadan/yolov4-deepsort/blob/3d4ef1627a828f894b74b754df9a5db3ada3584a/object_tracker_logonew.py) : Implements yolov4 + deepsort + DeepLogo for realtime detection according to the algo B given in the algo.md files
        - Ouputs a dict containing object , their ids and detected logo
- Imp Files in Deep Logo
    - [single_inf.py](https://github.com/mananmadan/DeepLogo/blob/master/single_inf.py) : contains all the function that is used with the object tracker files to detect logo .. (Stands for single inference!)
    - [annotations/](https://github.com/mananmadan/DeepLogo/tree/master/annotations): contains the dataset info (train,test classes distribution).Also has a parser to read through the annotation files
    - [imgs/](https://github.com/mananmadan/DeepLogo/tree/master/imgs): contains the custom dataset for testing the model
    - [MODEL-PERFORMARMANCE.md](https://github.com/mananmadan/DeepLogo/blob/master/MODEL-PERFORMANCE.md) : Contains the info about the testing process of the model and about the results
    - Testing Process and Notebook Demonstrating Working of Logo Detection
        - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1KOZ71GZXCz3N652kl832H_FfWX8K4Tx3?usp=sharing)

### Algos
- Read [algo.md](https://github.com/mananmadan/object-logo-detection/blob/master/algo.md)
