# TransmissionLineMonitoring

# CREATING DATASETS

To create an Transmission line monitoring AI using UAV, we first need to collect datasets.
To obtain datasets of transmission line,
We manually labeled the images of suspesion disc, vegetation stuck at conductors and so on.
To label the images and get annotation We used makesense.ai which is one of the best and fastest AI annotation website out there.

![sun-setting-silhouette-electricity-pylons](https://user-images.githubusercontent.com/70265297/154806515-833a1591-1f0a-46dd-8239-2ff190bd772b.jpg)


# Splitting datasets
Once we get our datasets we have to split our datasets into train and test which we will require when training our model.


# TRAINING
to create the object detection model, we will be using one of the pretrained AI model, :YOLOV5 you can see the documentation of yolo to get the detail knowledge of its architecure.

first you have to clone the whole YOLOV5 repository.
To clone the repository use the following code in cmd which is in the path that you want to clone the repository on :
cmd code : git clone https://github.com/ultralytics/yolov5 

**NOTE YOU MUST INSTALL GIT FOR ABOVE CODE TO RUN**

Now before jumping into training, we have to create a virtual environment so it doesn't clutter our PC with many versions of the same module

**To create a virtual env **

Use the cmd code : python -m venv VirtualEnvName

**To activate the environment**

Cmd code : .\VirtualEnvName\scripts\activate

Now once the virtual Environment is set up , go inside the yolov5 path , cmd code : cd PATH_TO_YOLOV5, example cd C:\desktop\YOLOv5

Then we have to install the neccessary modules which can be done by requirements.txt given in YOLOv5

CODE : pip install -r requirements.txt

# TRAINING IN YOLO V5

inside yolov5 create data.yaml  , remember the extension should be YAML
Now to train , change the nc which means number of classes, and in the list add the classes,
Use similar format , found inside coco.yaml give the path of train and test datasets then train. And ENJOY

THIS IS OUR TRAINED AI WHICH CAN DETECT SUSPENSION DISC, VEGETATION SHORT, AND TRANSFORMER

LATER WE WILL CONTINUE THIS PROJECT TO CREATE A CNN NETWORK TO CLASSIFY WHETHER THE DETECTED IMAGE SECTION IS FAULTY OR NOT.
STAY TUNED!!!!!

![val_batch0_labels](https://user-images.githubusercontent.com/70265297/154807171-60502699-b2d9-44eb-9157-111d3ef88375.jpg)

![train_batch2](https://user-images.githubusercontent.com/70265297/154807174-b830064e-d6e9-4e25-afe8-19170a4b936e.jpg)







