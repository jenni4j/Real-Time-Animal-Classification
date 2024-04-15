# Real Time Image Classification on Raspberry Pi 4

This repo is the software component of a Vertically Integrated Project at Georgia Tech with a goal of designing and implementing a device that distributes vaccine biscuits to foxes on campus when detected by a camera. 

#### Image Classification on a Raspberry Pi
The first step was setting up the Raspberry Pi device to run a pretrained MobileNetV2 model in order to perform real time image classification. MobileNetV2 has been pretrained on ImageNet, a dataset which has 1000 different image classes and includes animals such as foxes. The demo of the device performing image classification can be viewed in the file 'object-detection-demo.mov'. The script that was loaded and used on the Raspberry Pi device is named 'pretrained_model.py'. 

#### Fine-tuning Model with Fox Images
The second step was fine-tuning the model with fox images captured by a camera set up in a location on campus by previous semester students. The challenge was that we only had ~200 images of foxes of various quality, which likely meant that any fine-tuning would result in overfitting to the original dataset. Regardless, the notebook 'finetune.ipynb' showcases the steps taken to fine-tune the model with the data we had. Next semester's goal will be to find additional datasets of fox images that will allow us to more successfully fine-tune a model. 
