# Ayurvedic-plant-Recognition-using-YoloV3-model
This project is based on ayurvedic plants(medicinal purposes). As we know there are many plants are available in the surround and we don't know which plant has what specifications for use. So I have created a Machine Learning (image recognition) model which can able to detect and recognize the plant by the leaf image and give the information about the plant, which is present in the data. The model has trained with 280 images having 6000 epochs in the custom yoloV3 cfg file. The accuracy of the model is around 9.45334 for images predications.
In the GITHUB you will be able to find the codes of data categorizing, predication and plant dataset, training code for yoloV3, and all required files. Image annotation software is also there in the GitHub and config (.cfg) file of yoloV3.
There are some changes you should remember before training.
When you upload the classes.txt. After uploading again open the file on your pc/laptop and save it with file extensions called (.names). They should be named as classes.names . This file is used to label the image by the classes while training the model. After creating it upload it to the images folder. 
1. In training_model code, there is code of line which is used to create train.txt, test.txt, labelled_data.data . Please cross-check whether these files are there or not in the image folder. In train.txt and test.txt there will be the path of images for training. To see these files, I have uploaded my files for reference in files for the training folder.
2. Create a backup named folder in the drive where all the folders of images and darknet are located 
3. Cross-check the changes in the make file after running the code in training_model.
4. You have to do some major changes to the custom yolov3 file. In the darknet folder, there is a folder named cfg , where you have to find the yolov3.cfg file and rename it as you want. Open this file in the drive,/ text editor and there you have to do some changes. 
   1. you have uncommented some lines of testing and training, and put some numbers according to your dataset division in batch and subdivisions. 
   2. Then find the (max_batches=) in it and put some numbers for running the epochs (3000 if you're using collab because of runtime disconnection). Add some numbers in (steps=) between the max_batches numbers (the difference should be around 20 to 30). 
   3. Search Yolo in the find command. There you will find the (filter=) and put the value as per this formula [filter = (number of classes +5)*3]. There is one more chance you have to do in  [classes = (number of classes in classes.txt file)]. These two changes you have to for 3 in the .cfg file.
6. The model will automatically save in the backup folder along with the graph of epochs. The model will save in .weights extension.
7. If the darknet function is not running in collab. There is a code-named cmd, which will give pass access to this function.
To download the model the drive link is given bellow:
https://drive.google.com/drive/u/0/folders/1K3z05Eca0Yzba2BhklydU8s4BBySDon8 
