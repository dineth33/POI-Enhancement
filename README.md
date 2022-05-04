# POI-Enhancement

This repo contains materials to enhance the Point of Interest (POI) data for trip purpose inference using machine learning techniques. 

Two common issues of POI data which affects in trip purpose inference negatively are addressed. 

### 1. Improving the POI purpose categorization with text classification. 

<b> Problem: </b> 

POI data that can be extracted from different APIs mostly lack the category type for some which make the inference results useless.  

<b> Proposed Solution: </b> 

Intuitively, this issue can be solved using text classification as a model can be built to predict the category type based on the name of that POI. Simply put, when a POI has a name as “National Primary School”, there is a possibility that its purpose can be predicted as “educational”. 

K-Nearest Neighbors (KNN), Logistics Regression (LR), Random Forest (RF), Multinomial Naive Bayes (MNB), and Support Vector Machine (SVM) as conventional machine learning classifiers  and Convolutional Neural Network (CNN), Long Short-Term Memory (LSTM), Temporal Convolutional Network (TCN) as deep learning classifiers were evaluated to predict the purpose of a POI based on the name. 

Following table indicate the achieved F1-scores from each classifier. 





It was decided to continue with SVM as it provides a considerably higher accuracy with a lower computational time.


### 2. Identifying the possible entering locations for POIs with large land areas. 

<b> Problem: </b> 

There are POIs that are highly attractive but located far from the roads due to the large land areas of those such as schools, conference halls, and hospitals. This becomes an issue in purpose inference as the given location does not fall within the provided Walking Radius (R) around the DOP of a trip. 




<b> Proposed Solution: </b> 

Identifying the entrance locations of these POIs helps to reduce this issue. The proposed method is two fold as: (1) Prerequisite: Identifying the POIs which requires entrance locations, (2) Identfiying the entrance locations. [Click Here](#introduction-to-computer-science)








### Asssessing the impact of Enhanced POIs for trip purpose inference 

The trip purpose inference model developed by  (Gong et al.())  and developed by (Dhananjaya et al. ())  based on the Bayesian modeling is used in this study to access the impact of the suggested improvements. [Click Here](#introduction-to-computer-science)




### Acknowledgement 
<hr> 
This research was supported by the Accelerating Higher Education Expansion and Development (AHEAD) Operation of the Ministry of Higher
Education funded by the World Bank