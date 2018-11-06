
__[ <font color='black' size='4'> F. Alakwaa, et al. “Lilikoi: an R package for personalized pathway-based classification modeling using metabolomics data,” bioRxiv, 2018](https://www.biorxiv.org/content/early/2018/03/16/283408)__
    
https://www.biorxiv.org/content/early/2018/03/16/283408

<font color='black' size='4'>Lilikoi is a novel tool for personalized pathway analysis of metabolomics data.                      
 Lilikoi computes the pathway deregulation score for a given set of metabolites, selects the pathways with the highest mutual information and then uses them to build a classifier.

 <font color='red' size='5'>  Lilikoi has four modules </font> 

<font color='black' size='3'>
1. Feature mapping module, which standardizes the metabolite names provided by users, and map them to pathways. 
2. Dimension transformation module, which transforms the metabolomic profiles to personalized pathway-based profiles using pathway deregulation scores (PDS). 
3. Feature selection module which helps to select the significant pathway features related to the disease phenotypes, 
4. Classification and prediction module which offers various machine-learning classification algorithms.

![Image of Block Diagram](http://fadhl-alakwa.weebly.com/uploads/5/3/6/4/5364958/figure-1-1_orig.png)

Figure 1: The workflow of Lilikoi package. Lilikoi composed of four modules: Feature Mapper; Dimension Transformer; Feature Selector; and Classification Predictor. 

 <font color='blue' size='5'>  resources </font> 
1. __[Shiny Version](http://lilikoi.garmiregroup.org)__ http://lilikoi.garmiregroup.org
2. __[Example](https://github.com/lanagarmire/lilikoi/blob/master/lilikoi_example.ipynb)__
3. __[mybinder](https://mybinder.org/v2/gh/FADHLyemen/lilikoi_Fadhl/master)__
4. __[Docker](https://hub.docker.com/r/fadhlyemen/lilikoi/)__https://hub.docker.com/r/fadhlyemen/lilikoi/
5. __[CRAN](https://cran.r-project.org/web/packages/lilikoi/index.html)__ https://cran.r-project.org/web/packages/lilikoi/index.html
6. __[Github](https://github.com/lanagarmire/lilikoi)__ https://github.com/lanagarmire/lilikoi

![Image of Block Diagram](http://fadhl-alakwa.weebly.com/uploads/5/3/6/4/5364958/fig2-1_orig.png)

Figure. 2 The workflow of Module 1: Feature mapper. User can input any metabolite IDs such as chemical name, KEGG, PubChem and HMDB IDs. Fuzzy matching algorithm is implemented to map the non-matched names to the 100k synonyms database.  

![Image of Block Diagram](http://fadhl-alakwa.weebly.com/uploads/5/3/6/4/5364958/fig3-1_orig.png)

Figure 3. Heatmap of the individual-based pathway dysregulation scores (PDS) generated by Lilikoi. The rows are the pathway IDs, and the columns are the patients separated by group. PDS score is a personalized pathway metric ranging from 0 to 1. Higher PDS score indicates more dysregulation. (A) data set 1, breast cancer vs. healthy control plasma samples. (B) Data set 2, ER+ vs ER- breast cancer tissue samples. 

![Image of Block Diagram1](http://fadhl-alakwa.weebly.com/uploads/5/3/6/4/5364958/fig4-1_orig.png)

Figure 4. Measurements of selected pathway features in the two exemplary data sets. (A-B) data set 1, breast cancer vs. healthy control plasma samples. (C-D) data set 2, ER+ vs ER- breast cancer tissue samples.  (A, C) Selected pathway features measured by Information Gain, before constructing the classification models. The x-axis represents information gain score that measures the importance of the pathways, and y-axis displays the names of pathways selected from the training data. (B, D). Heatmap of selected pathway features measured by importance score, after constructing the classification models. The importance score is ranged from 0 (blue color) to 1 (red color). The seven machine learning methods from left to right are: recursive partitioning and regression analysis (RPART), linear discriminate analysis (LDA), support vector machine (SVM), random forest (RF), generalized boosted model (GBM), prediction analysis for microarray (PAM), and logistic regression (LOG).  

![Image of Block Diagram1](http://fadhl-alakwa.weebly.com/uploads/5/3/6/4/5364958/fig5-1_orig.png)

Figure 5. Model evaluation on the two exemplary data sets. (A-C) data set 1, breast cancer vs. healthy control plasma samples. (D-F) data set 2, ER+ vs ER- breast cancer tissue samples. (A, D) ROC curves of the breast cancer diagnosis testing set, obtained from seven classification algorithms: recursive partitioning and regression analysis (RPART), linear discriminate analysis (LDA), support vector machine (SVM), random forest (RF), generalized boosted model (GBM), prediction analysis for microarray (PAM), and logistic regression (LOG).  (B, E) Metrics (AUC, Sensitivity, Specificity and F-1 Statistic) to measure the performance of classification on training or testing data? (C, F). Metrics of the best-performing model on testing data, based on the criteria chosen by user (AUC in this case). 

![image ](http://fadhl-alakwa.weebly.com/uploads/5/3/6/4/5364958/fig6-1_orig.png)

Figure 6: Calibration of metabolomics model on data set 1 by confounding.  (A) ROC curves of metabolomics only, clinical data only, and metabolomics clinical combined model.  (B) Correlation coefficients among demographical/physiological factors and the metabolomics data. Blue colors indicates positive correlations and red indicated negative correlations
