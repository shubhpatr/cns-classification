# CNS Classification Report

Summary of all Models

![alt text](https://github.com/shubhpatr/cns-classification/blob/main/plots/table.JPG)



## Visualization Task

![alt text](https://github.com/shubhpatr/cns-classification/blob/main/plots/tsne.JPG)

Code is given in visualization.py

## Summary and Predictions of Models

Baseline Model

The model doesn't learn anything useful after a few predictions.
![alt text](https://github.com/shubhpatr/cns-classification/blob/main/plots/baselineTR.JPG)


Always predicts 6. 

For test dataset, predictions = 6,6,6,6,6

![alt text](https://github.com/shubhpatr/cns-classification/blob/main/plots/baselinehist.png)



VGG Model

Model performs well few epochs in, accuracy improves till 96% for test dataset. 
![alt text](https://github.com/shubhpatr/cns-classification/blob/main/plots/vgg.JPG)

Makes intelligent predictions
For test dataset, predictions = 0,0,1,1,1,6,2,2,2,2,2,2,2,2,2,2,2,2,2,3,3,3,6,2,5,5,5,5,5,6,10,10,6,6,6,6,6,6,6,6,6,6,6,6,10,6,6,10,6,6,6,6,8,2,8,3,6,10,10,10

![alt text](https://github.com/shubhpatr/cns-classification/blob/main/plots/vgghist.png)
Resnet Model

Model performs very slow while training, performance doesn't improve. 

Mostly predicts  6 like baseline
For test dataset, predictions = 6,6,6,6,6,6,10,6,6,6,6,6,6,6,10,6,6,6,6,6,6,6,6,10,10,10,10,10,10,6,6,6,6,10,6,6,6,6,6,6,6,10,6,6,6,6,6,6,6,6,6,6,6,6,6,6,6,6,6,6

![alt text](https://github.com/shubhpatr/cns-classification/blob/main/plots/resnethist.png)

Inception Model

Model performs well with training data. 


Makes intelligent predictions, though incorrect
For test dataset, predictions = 0,0,1,1,6,6,2,2,8,8,2,2,2,2,2,6,8,2,2,3,2,6,4,8,5,5,5,5,5,6,6,6,0,6,8,6,6,10,10,6,8,6,6,6,4,2,2,6,6,6,6,2,8,8,8,6,4,2,6,10
![alt text](https://github.com/shubhpatr/cns-classification/blob/main/plots/incepthist.png)

### Observations

* Used Data Augmentation, to populate the scarce training dataset, using rotations and adding noised
* Class Imbalance, mitigated using class weights

### Why some Images are classified incorrectly?

This is primarily due to the limited dataset, even with augmentation, we have just one image for training for few tissue types, this makes it challenging to model that will accurrately predict for each class. 
