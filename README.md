# X-Ray Classification of Pneumonia
### Classification model for St. Jude's Children's Hospital

## Project Overview:
Pneumonia affects nearly one out of every fifteen people worldwide annually. For most people contracting pneumonia isn't life threatening but of the near half billion people that contract it 2.5 million pass from this totally treatable illness. At most risk are seniors and children under 5 years old, for these people it is important to identify this illness in it's early stages before it has time to develop into a life threating situation.

## Business Problem:
St. Jude's Children's Hospital recognizes that in America pneumonia is not a leading cause of death in children but that world-wide every 43 seconds a child dies of this treatable disease. Most of these deaths are taking place in countries of Sub-Saharan Africa like the Congo, Guinea, and the Central African Republic.

By partnering with Europa, a company who specializes in handhelp X-Ray machines, St. Jude's plans on sending simple laptops and handheld X-Ray machines to countries with high mortality rates related to pneunomia. 

Due to a lack of medical staff who can properly identify pneumonia St. Judes has asked us to build a machine learning model that can quickly and accurately identify pneumonia with x-ray images.

## Data Understanding
Our model has been trained off of nearly 6,000 chest X-Ray's supplied to us through [Kaggle.com](https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia). This data was originally gathered by the Guangzhou Women and Children’s Medical Center and consist of X-Ray's of children one to five years of age. The original set has a class imbalance of 1(Normal):2.7(Pneumonia). Origianlly split into a train, test and validation with a surprisingly low validation set size of only 16 images we chose to rebalance it to a ratio to .65/.2/.15.  

## Modeling and Results:
Throughout this process we were tasked with identifying if an image was that of pneumonia. By iterating through multiple versions of a Convolutional Neural Network we were able to build a model to make this classification. After using our training data to form our model and our validation set to confirm it's fitting we ran our testing data through to confirm our final results. After seven iterations we were satisfied with the results of our model. On unseen data our final model accuracy is 95% and has a recall of 98%. Compared to our dummy model with an accuracy of 75% this is a sizeable increase.

## Evaluation:
We chose to go with a model that performs best in recall. Recall will lead to more false positive (where someone is identified as having pneumonia when they do not) assertions of pneumonia but because a false positive is less consequential than a false negative (when someone with pneumonia is told they  do not have pneumonia) it is a the best metric in this case. 

For our next steps we would be able to augment our image data to create more images to train our model on. Given more time we may, through more tweaking of the hyper parameters, be able to find a more successful model. Our final step is to get the model and the portable X-Ray machines into the hands of people who need them.
