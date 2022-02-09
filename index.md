# Multi Object Detection with YOLO on Artwork Dataset
- `Report_Yihui.pdf` is my Report  
- `code` Folder include my codes  
- `resource` Folder are some references  

###### Below are just some notes

# writeup
- [x] dataset
- [x] features
- [x] partition
- [x] classification scheme
- [x] cross validation
- [x] precision vs recall
- [x] accuracy
- [x] lessons learned

#faster RCNN  
RCNN  
- Spatial pyramid pooling  
- Region proposal  

### useful link  
[Tutorial on Tools for Efficient Object Detection](http://mp7.watson.ibm.com/ICCV2015/ObjectDetectionICCV2015.html)

### segmentation  
#### Kmeans  
#### mean shift
#### Graph
If external diff > minimal internal, different graphs.  
Then run greedy based on edge weight 3 times for R,G,B.  
Gradually merge pixels.    

#### Distance measure:  
- Nearest neghbor  
- 8 neighbors around one pixel  

### Localization  
- HoG  
- SIFT  
- “neocognitron”  
- sliding window  

### bounding box regression  
What is backgound windows?  

use the pool5 features to compute a new bounding box?  
Make bbox bigger towards the ground truth.  


### detection  
- latent SVM  
- convNet  

### Classifier  
- softmax
- SVM  
- KNN?  

### ablation study  
pool5 is better than fc6 without fine-tuning  
fc sort of stands for domain specified knowledges  

### evaluation  
- mean average precision  
- detection analysis tool  

### visualization  
- using first layer  
- single out a feature and figure out all max response pictures  

### other approach  
- overfeat  
- spatial pyramid  


### RCNN main steps
1. Generate regions using selective search
2. Extract features on each region
3. classification on features
4. one class bounding box regression on features
5. non-maximum suppression
http://videolectures.net/iccv2015_girshick_fast_r_cnn/
