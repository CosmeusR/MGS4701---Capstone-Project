# Project---Analyzing the Game: Predicting Pro Bowl NFL Quarterbacks Using Performance Metrics
This repository contains our business analytics project on NFL quarterback performance and Pro Bowl selection. The project examines whether quarterback statistics alone can help explain which players are selected to the Pro Bowl, while also recognizing that outside factors such as fan voting, media attention, team success, and popularity can influence the final outcome.
**Objective**
The objective of this study is to develop a predictive model that determines whether an NFL quarterback will be selected to the Pro Bowl based on performance metrics. The project aims to identify key statistical variables, build a predictive measure, evaluate model accuracy, and examine how traditional and advanced quarterback metrics contribute to Pro Bowl recognition.
**Dataset**
The dataset was obtained from Kaggle and includes NFL quarterback passing data from 2001 to 2023. It covers 2,351 observations. The target variable is Pro Bowl selection, where 1 represents selected and 0 represents not selected. The primary predictor variables used in the final model are passing yards, touchdowns, interceptions, completions, passer rating, and Adjusted Net Yards per Attempt (ANY/A).
**Methodology**
Before analysis, the dataset was cleaned and preprocessed to improve consistency and reduce unnecessary noise and duplicate data. Missing values were handled using median imputation. Outliers were treated using the interquartile range method for numerical variables, while the binary target variable was excluded from that process. Aggregate team rows were removed, and sack-related variables were dropped because they were not essential to evaluating quarterback passing performance. Exploratory analysis included histograms, boxplots, scatter plots, correlation heatmaps, and crosstab analysis to examine variable distributions and relationships.
The report treats Pro Bowl selection as a binary classification task and uses logistic regression as the primary predictive model. After cleaning the dataset, the data were split into training and testing sets using an 80/20 split. Model performance was evaluated using accuracy, a confusion matrix, precision, recall, and F1-score. Additional evaluation was performed using ROC-AUC, and Principal Component Analysis (PCA) was used to examine how much of the variation in quarterback performance could be explained by a smaller number of components.
**Analysis and Results**
The logistic regression model produced strong overall results. It achieved an accuracy score of 94.61%, showing that it correctly classified most quarterbacks as either Pro Bowl selections or non-selections. The confusion matrix showed that 418 quarterbacks were correctly identified as not selected and 21 were correctly identified as selected, while 10 were false positives and 15 were false negatives. The classification report showed that the model performed much better on non-selections than selections, with the Pro Bowl class recording 0.68 precision, 0.58 recall, and an F1-score of 0.63. These results suggest that while the model was effective overall, it was still less consistent when identifying quarterbacks who actually made the Pro Bowl.

The coefficient analysis showed that certain variables had a stronger influence on Pro Bowl selection than others. Touchdowns, quarterback rating, and ANY/A positively affected a quarterback’s chances of being selected, while interceptions negatively affected those chances. This suggests that both traditional and advanced quarterback metrics are important in evaluating overall performance.

The ROC-AUC analysis was used as a secondary measure beyond the base model results. The model produced an AUC score of 0.959, showing strong classification performance and strong separation between quarterbacks who were selected to the Pro Bowl and those who were not. The ROC curve also showed that the model kept the false positive rate relatively low while maintaining a strong true positive rate across different thresholds.

The PCA results showed that the first principal component explained 65.13% of the total variance and the second principal component explained 29.88%. Together, the first two components accounted for approximately 95% of the dataset’s variation. The first component represented overall passing production, while the second reflected passing efficiency.<img width="848" height="468" alt="Passing Yards" src="https://github.com/user-attachments/assets/7ebfedee-84b4-4d25-94a5-cbd51ea337f3" />



**Discussion**
The findings of this study show that quarterback performance metrics provide meaningful predictive value when it comes to Pro Bowl selection. Statistical performance served as a strong foundation for evaluating Pro Bowl-level quarterback play, particularly through passing production and efficiency. At the same time, the study also showed that performance metrics alone do not fully explain Pro Bowl outcomes. Pro Bowl recognition is not based only on on-field production, since fan voting, media attention, team record, popularity, and narrative can also influence who ultimately receives recognition.

Still, a model like this can help make Pro Bowl evaluation more consistent by establishing a clearer statistical benchmark for what counts as Pro Bowl-level quarterback performance. It can help identify the traits most closely tied to true Pro Bowl talent and reduce the chance of relying too heavily on outside factors such as reputation or popularity. In that sense, the model can serve as a more objective tool for recognizing quarterbacks whose production and efficiency reflect the level expected of a Pro Bowl player.

**Tools Used**
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

**Authors**
- Reginald Cosmeus & Tochukwu Maduagwu
