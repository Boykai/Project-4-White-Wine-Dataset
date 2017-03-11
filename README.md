# Prject-4-White-Wine-Dataset
## White Wine Dataset - Explore and Summarize Data 
#### By James Tooles

## Introduction of White Wine Dataset Section
This dataset 'White Wine Quality', was aquired from [Udacity Pre-created Datasets](https://docs.google.com/document/d/1qEcwltBMlRYZT-l699-71TzInWfk4W9q5rTCSvDVMpc/pub?embedded=true). 

The documentation for most of the dataset is included below throughout the analysis. The following could aid with the introduction of the White Wine Quality dataset, [documentation information](https://s3.amazonaws.com/udacity-hosted-downloads/ud651/wineQualityInfo.txt).

### Past Usage:

  P. Cortez, A. Cerdeira, F. Almeida, T. Matos and J. Reis. 
  Modeling wine preferences by data mining from physicochemical properties.
  In Decision Support Systems, Elsevier, 47(4):547-553. ISSN: 0167-9236.

  In the above reference, two datasets were created, using red and white wine samples.
  The inputs include objective tests (e.g. PH values) and the output is based on sensory data
  (median of at least 3 evaluations made by wine experts). Each expert graded the wine quality 
  between 0 (very bad) and 10 (very excellent). Several data mining methods were applied to model
  these datasets under a regression approach. The support vector machine model achieved the
  best results. Several metrics were computed: MAD, confusion matrix for a fixed error tolerance (T),
  etc. Also, we plot the relative importances of the input variables (as measured by a sensitivity
  analysis procedure).
  
### Relevant Information:

   The two datasets are related to red and white variants of the Portuguese "Vinho Verde" wine.
   For more details, consult: http://www.vinhoverde.pt/en/ or the reference [Cortez et al., 2009].
   Due to privacy and logistic issues, only physicochemical (inputs) and sensory (the output) variables 
   are available (e.g. there is no data about grape types, wine brand, wine selling price, etc.).

   These datasets can be viewed as classification or regression tasks.
   The classes are ordered and not balanced (e.g. there are munch more normal wines than
   excellent or poor ones). Outlier detection algorithms could be used to detect the few excellent
   or poor wines. Also, we are not sure if all input variables are relevant. So
   it could be interesting to test feature selection methods. 
   
### Attribute information:

   For more information, read [Cortez et al., 2009].

   Input variables (based on physicochemical tests):
     
     1. - fixed acidity (tartaric acid - g / dm^3) 
     
     2. - volatile acidity (acetic acid - g / dm^3)
     
     3. - citric acid (g / dm^3)
     
     4. - residual sugar (g / dm^3)
     
     5. - chlorides (sodium chloride - g / dm^3
     
     6. - free sulfur dioxide (mg / dm^3)
     
     7. - total sulfur dioxide (mg / dm^3)
     
     8. - density (g / cm^3)
     
     9. - pH
     
     10. - sulphates (potassium sulphate - g / dm3)
     
     11. - alcohol (% by volume)
     
     * Output variable (based on sensory data): 
     
     12. - quality (score between 0 and 10)
   
### Missing Attribute Values: None

### Description of attributes:

   1 - fixed acidity: most acids involved with wine or fixed or nonvolatile (do not evaporate readily)

   2 - volatile acidity: the amount of acetic acid in wine, which at too high of levels can lead to an unpleasant, vinegar taste

   3 - citric acid: found in small quantities, citric acid can add 'freshness' and flavor to wines

   4 - residual sugar: the amount of sugar remaining after fermentation stops, it's rare to find wines with less than 1 gram/liter and wines with greater than 45 grams/liter are considered sweet

   5 - chlorides: the amount of salt in the wine

   6 - free sulfur dioxide: the free form of SO2 exists in equilibrium between molecular SO2 (as a dissolved gas) and bisulfite ion; it prevents microbial growth and the oxidation of wine

   7 - total sulfur dioxide: amount of free and bound forms of S02; in low concentrations, SO2 is mostly undetectable in wine, but at free SO2 concentrations over 50 ppm, SO2 becomes evident in the nose and taste of wine

   8 - density: the density of water is close to that of water depending on the percent alcohol and sugar content

   9 - pH: describes how acidic or basic a wine is on a scale from 0 (very acidic) to 14 (very basic); most wines are between 3-4 on the pH scale

   10 - sulphates: a wine additive which can contribute to sulfur dioxide gas (S02) levels, wich acts as an antimicrobial and antioxidant

   11 - alcohol: the percent alcohol content of the wine

   Output variable (based on sensory data): 
   12 - quality (score between 0 and 10)

## Univariate Plots Section
The White Wine dataset consists of 13 variables, with almost 5,000 observations.

Starting with a default histogram of the 'quality' feature within the 'wine' dataset resembles a Gaussian distribution of the 'quality' feature, centered at a 'quality' value of 6. By increasing the bin size of the histogram allowed a better visual depiction of the dataset, which is slightly positively skewed. These graphs support the findings within the statistical summary for 'quality' with a median value of 6, and a mean value of 5.878.

The dataset documentation states that the 'quality' feature should range from 0-10, unfortunately all of the wines within this dataset range from 3-9.

## Univariate Analysis


#### What is the structure of your dataset?
There are 4898 wines of 13 features (x, fixed.acidity, volatile.acidity, citric.acid, residual.sugar, chlorides, free.sulfur.dioxide, total.sulfur.dioxide, density, pH, sulphates, alcohol, quality). All of these variables are given as quantitative variables.

* **X**: a unique id identifier for each wine

* **fixed acidity**: most acids involved with wine or fixed or nonvolatile (do not evaporate readily)

* **volatile acidity**: the amount of acetic acid in wine, which at too high of levels can lead to an unpleasant, vinegar taste

* **citric acid**: found in small quantities, citric acid can add 'freshness' and flavor to wines

* **residual sugar**: the amount of sugar remaining after fermentation stops, it's rare to find wines with less than 1 gram/liter and wines with greater than 45 grams/liter are considered sweet

* **chlorides**: the amount of salt in the wine

* **free sulfur dioxide**: the free form of SO2 exists in equilibrium between molecular SO2 (as a dissolved gas) and bisulfite ion; it prevents microbial growth and the oxidation of wine

* **total sulfur dioxide**: amount of free and bound forms of S02; in low concentrations, SO2 is mostly undetectable in wine, but at free SO2 concentrations over 50 ppm, SO2 becomes evident in the nose and taste of wine

* **density**: the density of water is close to that of water depending on the percent alcohol and sugar content

* **pH**: describes how acidic or basic a wine is on a scale from 0 (very acidic) to 14 (very basic); most wines are between 3-4 on the pH scale

* **sulphates**: a wine additive which can contribute to sulfur dioxide gas (S02) levels, which acts as an antimicrobial and antioxidant

* **alcohol**: the percent alcohol content of the wine

* **quality** (score between 0 and 10)
    * (worst) 0 -------> 10 (best)

Other observations:

* The 'quality' distribution is approximately normal
* The median 'quality' value is 6.0
* Citric acid has a spike in wine count at a value of 0.5

#### What are the main features of interest in your dataset?
The main features of interest are any features that significantly contribute to the quality output value. The goal of this analysis is to determine which features are best for predicting the quality of a wine.

#### What other features in the dataset do you think will help support your investigation into your feature of interest?
Volatile acidity, citric acid, residual sugar, chlorides, total sulfur dioxide, pH, and alcohol. All of these features are described in the dataset documentation as to affect the taste, smell, or other measurements of value to consumers such as alcohol content.

The other features such as, fixed acidity, free sulfur dioxide, density, sulphates, do not seem to play a role in determining quality value due to the description given within the dataset documentation. All of these features are either dependent upon other features of interest, preservatives, or do not show enough variance to be heavily weighted in determining wine quality.

#### Did you create any new variables from existing variables in the dataset?
Yes, a categorical feature of quality was created called 'quality.cat'.

#### Of the features you investigated, were there any unusual distributions? Did you perform any operations on the data to tidy, adjust, or change the form of the data? If so, why did you do this?
The citric acid feature has a spike in wine count at a value of 0.5, this seems odd and interesting and will be investigated for any impact in wine quality within the bivariate section.

All of the features were limited, outliers removed, and/or parsed in more visual detail to see any hidden attributes within the feature.

The quality feature, was shown on a bar graph to highlight the ordinal property of the feature.

## Bivariate Plots Section

From a subset of the citric acid, residual sugar, and pH do not seem to have strong correlations with quality, but volatile acidity, chlorides, total sulfur dioxide, density, and alcohol are moderately correlated with quality. I want to look closer at scatter plots involving quality and some other variables like volatile acidity, chlorides, density, and alcohol.

The high quality wines have a low volatile acidity value, only the sub-par wines have high volatile acidity values. This analysis only tells us part of the story given the correlation value of -0.195 for quality vs volatile acidity.

The majority of wines have low chlorides values. The high quality wines have a low chlorides value; a large number of average wines have high chlorides values. There are a few outliers on the high quality and low quality wines with a large chlorides value. This analysis only tells us part of the story given the correlation value of -0.210 for quality vs chlorides.

As the quality of the wines increase, the limits for total sulfur dioxide values seem to converge from 80 to 140, with the low quality wines having a much larger variation of total sulfur dioxide values, about 20 to 280. This analysis only tells us part of the story given the correlation value of -0.175 for quality vs total sulfur dioxide.

The high quality wines have a low density value, only the sub-par wines have high density values. The density and quality of wine has a decent correlation value of -0.307. 

The high quality wines have a higher alcohol value, only the sub-par wines have lower alcohol values. Only a small portion of wines have high quality and low alcohol content. The quality and alcohol features have the highest correlation yet, at a value of 0.436.

As the alcohol values increase, the density decreases. This could be due to alcohol having a lower density than the rest of the wine content, therefore bringing down the overall density of the wine. Alcohol and density have a strong negative correlation value of -0.780.

The residual sugar and density have a strong positive correlation of 0.839. As the residual sugar increases, the density increases. This could be due to the fact that residual sugar has a higher density compared to the remaining wine content. This could also be related to the fact that during fermentation, sugar is turned into alcohol. So the less sugar turned into lower density alcohol, the higher the density of the wine.

The alcohol content and residual.sugar have a moderate negative correlation of -0.451. As the residual sugar increases, the alcohol content decreases. This is most likely due to the fermination process of making acohol, which consumes sugar to produce alcohol.


## Bivariate Analysis

#### Talk about some of the relationships you observed in this part of the investigation. How did the features of interest vary with other features in the dataset?
The relationship between volatile acidity and quality of wines has a parabolic shape, in the sense that the low and high quality wines have a higher level of volatile acidity, while the average wines have a lower volatile acidity.

For the chlorides levels, the chlorides values decrease as the quality of wine increases.

The total sulfur dioxide has one of the most interesting relationships to quality, as it converges to a total sulfur dioxide range of 80 to 140 as the quality of wine increases. The lower quality wines have a much larger variation of total sulfur dioxide values.

The wine density decreases as the wine quality increase, with a significant drop as the wine quality equals 9.

As the median alcohol level increases, the wine quality increases. The alcohol feature has the highest correlation with wine quality out of all of the given features.

#### Did you observe any interesting relationships between the other features (not the main features) of interest)?
The density, alcohol, and residual sugar features seem to be highly correlated with each other. The alcohol is created by consuming sugar during the fermentation process, and the more alcohol within the wine the lower the density of the wine given the density of the alcohol relative to residual sugar and the remaining wine content.

#### What was the strongest relationship you found?
The relationships between the wine features of density and alcohol, alcohol and residual sugar, residual sugar and alcohol, and alcohol and quality.


## Multivariate Plots Section

The first graph shows us the quality distribution as a function of color, plotted in a density vs alcohol graph. The graph is then separated to show the different trends per quality value. The wine quality starts at a value of 3, where the wines are grouped around high density and low alcohol values. As the wine quality increases, the points tend towards higher alcohol levels and lower density levels.

The residual sugar and density relationships have extremely high variation, except at the highest quality level. The majority of wine quality 9, have both low residual sugar and density.

The first graph shows us the quality distribution as a function of color, plotted in a alcohol vs residual sugar graph. The graph is then separated to show the different trends per quality value. The wine quality starts at a value of 3, where the wines are grouped around low alcohol and a variation of residual sugar values. As the wine quality increases, the points tend towards higher alcohol levels and lower residual sugar levels.

The linear model created has extremely low R-squared values. This could be due to the diversity of the dataset given in the original wine dataset. The majority of the data given has a wine quality value of 5, 6, 7. Shown in the quality bar graph in the Univariate section. Having a more diverse dataset would lead to a better modeling of the data.


## Multivariate Analysis

#### Talk about some of the relationships you observed in this part of the investigation. Were there features that strengthened each other in terms of looking at your feature of interest?
The density vs alcohol graph showing the quality of the wines was insightful. There seemed to be an overall trend, as you can see the shifting of plot points as the quality of wine increases.

The density vs residual sugar graph showing the quality of the wines, highlighted the variation of wines with low wine quality, while the high quality wines seemed to converge around a similar density/residual sugar ratio.

The alcohol vs residual sugar graph was a mix between the trends shown in the first two graphs in reference to the wine quality values. As the wine quality increased, the movement trend of the alcohol/residual sugar ratio was shown, as well as a decrease in variation of the feature values as the wine quality increased.

#### Were there any interesting or surprising interactions between features?
The general decrease in variation of the observed features as the wine quality increased was interesting. From this dataset it showed that as the wine quality increases the wine features converge to a given range of feature values, for the observed features.


#### OPTIONAL: Did you create any models with your dataset? Discuss the strengths and limitations of your model.

Yes, a linear model was created for this dataset. The reported R-squared values are extremely low. This is most likely due to the lack of variation within the dataset for the wine quality values. This dataset does not fair well for predictive linear models, when the output feature (wine quality) is so concentrated in <30% of the possible wine quality values.

------


## Final Plots and Summary
### Plot One
#### Description One
The distribution of wine qualities appears to be normal, centered around 6 but, due to the lack of variation in the wine quality feature, it was difficult to determine what contributes to a high quality or low quality wine, due to the majority of wines in this dataset having an average quality.

### Plot Two
#### Description Two
The average wine quality is over represented within this wine dataset but with the above graph it is clear that the majority of high quality wines tend to have high alcohol levels and low density levels.

### Plot Three
#### Description Three
The alcohol level of a wine by volume tends to be positively correlated and increase with the wine quality level. Generally, in the dataset given, the higher the median alcohol value, the higher the quality of wine.

## Conclusions
The white wine data set contains information on almost 5,000 wines, with 12 different features, and was created in 2009. I started by observing the distributions of each feature within the dataset. From there I took note of any trends, abnormalities, and possible insights into the meanings behind the features. I then started cross plotting and correlating the different features with quality, and some of the features with other input features given in the dataset. Finally, I explored the additive effects of features on the overall wine quality feature and created a linear model to better understand the dataset.

There was a clear trend with median alcohol content and wine quality. There were also clear trends with a combination of residual sugars, alcohol, density, and wine quality. Some of these variables could be dependent upon each other, more domain knowledge is needed for further insight into the data exploration. The relationships between the afore mentioned features became more clear, when scatter plots were created, and separated by wine quality. The plot points migrated, converged, and created a clear underlying relationship to the wine quality.

Unfortunately, the dataset given is heavily concentrated on average wine qualities. The lowest, and highest wine quality levels were sparse within this dataset. Giving way to a poor predictive linear model, with a low R-squared value, due to the lack of variation in the wine quality (output feature). This data could also be non-linear, feature incomplete, and otherwise not verbose enough to gain a more definitive model. Other machine learning models were not attempted, and a linear model might not be the best approach to modeling this dataset. For future work, a wider range of features for the wine, such as, price, age, location of production, and other features would greatly enrich the dataset. In the end, a median high alcohol percentage wine, gave way to a higher quality wine, other features could and do impact the wine quality value but, this feature trended strongly given the final box plot shown within this exploration.


## References

Citation Request:
  This dataset is public available for research. The details are described in [Cortez et al., 2009]. 
  Please include this citation if you plan to use this database:

  P. Cortez, A. Cerdeira, F. Almeida, T. Matos and J. Reis. 
  Modeling wine preferences by data mining from physicochemical properties.
  In Decision Support Systems, Elsevier, 47(4):547-553. ISSN: 0167-9236.

  Available at: [@Elsevier] http://dx.doi.org/10.1016/j.dss.2009.05.016
                [Pre-press (pdf)] http://www3.dsi.uminho.pt/pcortez/winequality09.pdf
                [bib] http://www3.dsi.uminho.pt/pcortez/dss09.bib
