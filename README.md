## Object and Logo Detection

### Installation and Running
- See in Colab Notebook
- [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1O84ALermB0Jh6MFe1mGAfFc1aP03eOae?usp=sharing)
- [Open in Jupyter](https://github.com/mananmadan/object-logo-detection/blob/master/Vision_Detection_System_(Video_%2B_DeepLogo)_Final.ipynb)

### File Structure
- Imp Files Modified in **Yolov4 + deepsort**
    - [INFO.md](https://github.com/mananmadan/yolov4-deepsort/blob/master/INFO.md): contains all the referenced and info about he model used for Yolov4 and deep sort
    - [object_tracker.py](https://github.com/mananmadan/yolov4-deepsort/blob/c336e0d3c0db085f958334d4d884f947b54972d4/object_tracker.py) : Implements yolov4 + deepsort and stores the segmented image of each object in a folder
    - [algoa.py](https://github.com/mananmadan/yolov4-deepsort/blob/c336e0d3c0db085f958334d4d884f947b54972d4/algoa.py) : Implements yolov4 + deepsort + DeepLogo for realtime detection according to the algo A as given in algo.md files
        - Outputs a Dict contains object , their ids and detected logo
    - [algob.py](https://github.com/mananmadan/yolov4-deepsort/blob/c336e0d3c0db085f958334d4d884f947b54972d4/algob.py) : Implements yolov4 + deepsort + DeepLogo for realtime detection according to the algo B given in the algo.md files
        - Ouputs a dict containing object , their ids and detected logo

- Imp Files in **Deep Logo**
    - [single_inf.py](https://github.com/mananmadan/DeepLogo/blob/9d1feeb2ec3e3a22d72cb6dbd9ca34b77243b294/single_inf.py): contains all the function that is used with the object tracker files to detect logo .. (Stands for single inference!)
    - [annotations/](https://github.com/mananmadan/DeepLogo/tree/master/annotations): contains the dataset info (train,test classes distribution).Also has a parser to read through the annotation files
    - [imgs/](https://github.com/mananmadan/DeepLogo/tree/c3d57d456d5d424c330bb16adcb3fa36f2ecc934/imgs): contains the custom dataset for testing the model
    - [MODEL-PERFORMARMANCE.md](https://github.com/mananmadan/DeepLogo/blob/master/MODEL-PERFORMANCE.md) : Contains the info about the testing process of the model and about the results
    - Testing Process and Notebook Demonstrating Working of Logo Detection
        - [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1KOZ71GZXCz3N652kl832H_FfWX8K4Tx3?usp=sharing)

### Algos
- Read [algo.md](https://github.com/mananmadan/object-logo-detection/blob/master/algo.md)


#### Algo A Flowchart
![Algo A](flowchart/algoa.jpeg)
- Open Graph with links
    - Might Require to create an account
    - [algoa-tech](https://lucid.app/lucidchart/invitations/accept/inv_46850663-752c-4443-a89e-9405daa3cb4e)

#### Algo B Flowchart
![Algo B](flowchart/algob.jpeg)
- Open Graph with links
    - Might Require to create an account
    - [algob-tech](https://lucid.app/lucidchart/invitations/accept/inv_25b733c3-49c2-4c5e-8cf2-10252f88a2d2?viewport_loc=868%2C667%2C2219%2C1129%2C0_0)

### Future Scope
- Train a single model to give object and the logo both?
- Add more diverse images .. as images of some classes like apple are not diverse enough
- Test More as to what qualilty of image yeilds best detection results .. then maybe apply some processing filtering techniques to make detection accurate (hence also faster)
- Research on Sequence based methods to process video?