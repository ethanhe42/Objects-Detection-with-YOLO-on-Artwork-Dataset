### training and validation 
#### environment requirement
darknet
#### steps  
0. Extract train folder 
1. Download PASCAL VOC 2007 and 2012 training, validation and testing sets.(about 3GB)  
2. put them into a `VOCdevkit` Folder.  
3. link `VOCdevkit` folder to the inside of `train` folder  
4. Then download [imagenet pretrained model](http://pjreddie.com/media/files/extraction.conv.weights)  
5. Then `./darknet partial cfg/extraction.cfg extraction.weights extraction.conv.weights 25`  
6. Then `./darknet yolo train cfg/myYOLO.cfg extraction.conv.weights`  
7. After 40,000 iterations, you're done.  

### testing
#### environment requirement
tensorflow, opencv2There
#### steps
To test my code, first you need to install tensorflow and opencv2.  
After that, Download my trained model from [my google drive](https://drive.google.com/file/d/0B_ayvzUASy9YeU8wTC16SFlXZzA/view?usp=sharing)
(About 1GB).  
Put the weights.ckpt into the `weights` folder.  
Then Download the testing pictures you wanna use.  
To run test on it  
`python main.py -fromfile image.jpg`  
