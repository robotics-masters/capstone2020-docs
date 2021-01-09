# CNN model evaluation 

- Author: Yiran 
- Date: 2 Oct 2020

This wiki page gives guides that how to evaluate the CNN model performance based on the training data, validation data, and test data. 

## Contents
- Criteria 1: No overfitting
- Criteria 2: High test accuracy
- Criteria 3: Looking confusion matrix
- Criteria 4: Looking classification report
- Criteria 5: Track the model performance using future data
- CNN model accuracy test on 2 Oct

### Criteria 1: No overfitting

Overfitting is "the production of an analysis that corresponds too closely or exactly to a particular set of data, and may therefore fail to fit additional data or predict future observations reliably"

To avoid overfitting, the test accuracy using new images (test data) should be close to the evaluation accuracy achieved during model training.

### Criteria 2: High test accuracy
Accuracy is the ratio of the number of correct predictions to the total number of input samples. We want high accuracy using the new data.


### Criteria 3: Looking confusion matrix and classification report

The confusion matrix shows the ways in which your classification model is confused when it makes predictions.

- Confusion matrix: Give the number of correct and incorrect predictions are summarized with count values and broken down by each class.  
- **Normalized Confusion Matrix**: A row represents an instance of the actual class (i.e. an actual surgical step), whereas a column represents an instance of the predicted class (i.e. the predicted surgical step). Consequently, the values of the diagonal elements represent the degree of correctly predicted classes. The confusion is expressed by the false classified off-diagonal elements since they are mistakenly confused with another class. 

Thus, we want higher numbers in the diagonal position. 


### Criteria 4: Looking classification report

We can also find the number of samples in the test data in the `support` column of the classification report. The `recall` is the true positive rate, `precision` is the rate of true positive to the total predicted positive. And the `f1 score` = 2*((precision*recall)/(precision+recall)), used when we select a model based on a balance between precision and recall. Thus, the higher the value of recall, precision, f1, the better. And we want all classes can get high f1 scores. 


### Criteria 5: Track the model performance using future data
To ensure the model is robust, we need to test the model based on the newly collected data. 


## **CNN model accuracy test on 2 Oct**
- [Jupyter notebook link for the CNN model testing](https://bitbucket.org/RobertJia/comp3988_t17b_group1/src/master/sign_detection_code/Yiran/Sign_Classification_2Oct.ipynb)
- [Link of the test data](https://drive.google.com/file/d/1ABoMF8V9I9DZlMJxaWx_9FfOXZ4jIgLj/view?usp=sharing)

The accuracy test is based on more than 1200 new images, which are not included in the model training. 

From the image below, we can see that:

1. The **overall accuracy is 93%**, which means that the model can classify 93% input images correctly. 
2. By looking the diagonal presicion of normalised confusion matrix, all classes get close to 95% accuracy, except relatively low value in the class `left` (75%). 
3. Most misclassifications are classified to "other" (i.e. no sign detected). 
4. The f1 score of all classes are more than 90%, except relatively low in the class `left`.


![Screen Shot 2020-10-02 at 7.39.58 pm.png](https://bitbucket.org/repo/G6xBMXK/images/1780032738-Screen%20Shot%202020-10-02%20at%207.39.58%20pm.png)