### Classifying skin abnomalities as malignate or benige

**Richard Higgs**

#### Executive summary
Skin abnormalities that are malignant have physical characteristics that can be used to distinguish them from benign features.  Those characteristics include shape, size and texture.  Using a dataset complied by YBI Foundation, I provide a model that provides a malignant or benign prediction.  The model is tuned to error on the side of caution.  It is more likely that benign abnormalities are classified as malignant than malignant abnormalities are classified as benign.  When a specific sample is classified as malignant, a biopsy should be conducted. 

#### Rationale
The model prediction is much quicker and cheaper than a biopsy.  It is also more objective and will give the same weight to abnormalities each time.  Predictions by a medical practitioner may vary from case to case.  Predictions may also vary with different practitioners.

#### Research Question
Should a provider conduct a biopsy of an abnomality?

#### Data Sources
https://www.kaggle.com/code/ybifoundation/cancer-prediction

The data consists of 10 attributes:
1.	radius (mean of distances from center to points on the perimeter)
2.	texture (standard deviation of gray-scale values)
3.	perimeter
4.	area
5.	smoothness (local variation in radius lengths)
6.	compactness (perimeter^2 / area - 1.0)
7.	concavity (severity of concave portions of the contour)
8.	concave points (number of concave portions of the contour)
9.	symmetry
10.	fractal dimension (coastline approximation - 1)
The mean, standard error and largest or worst values are included for each of the 10 attributes.


#### Methodology
I performed several types of classification techniques and found Logistic Regression gave the best results.  By using the probability values provided though the model with a threshold of 0.25, I was able to skew the results to avoid classifying abnormalities as benign when they are malignant.

#### Results
The data has only 569 entries.  While the model is tuned to return zero False-Negative results, I would think more data is needed to give confidence in the model.

#### Next steps
The current notebook has a lot of exploratory code.  The final notebook will include only the model and implementation of the current dataset.  A final product should include the means to add additional data and rerun the model.

#### Outline of project

[Link to notebook_mod20](https://github.com/rickhiggs/Capstone_Mod20/blob/main/CapstoneExplore02.ipynb)

[![LogReg.png](https://github.com/rickhiggs/Capstone_Mod20/blob/main/images/LogReg.png)](https://github.com/rickhiggs/Capstone_Mod20/blob/main/images)

[![LogRegWithThresh.png](https://github.com/rickhiggs/Capstone_Mod20/blob/main/images/LogRegWithThresh.png)](https://github.com/rickhiggs/Capstone_Mod20/blob/main/images)
- 
##### Contact and Further Information
**Richard Higgs**
rickhiggs@yahoo.com
