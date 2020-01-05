Research papers which have defined the concept of K modes and by extension K prototypes (as it is a mixture of k means and k modes) are:- 
1.	https://link.springer.com/article/10.1023/A:1009769707641
2.	https://grid.cs.gsu.edu/~wkim/index_files/papers/kprototype.pdf

This is an in depth description of the k prototypes clustering code file attached alongside. Both .ipynb and .py files have been attached. This is applicable for a particular unit code like Adilabad in this case.

The file takes as input a csv file from which duplicates have been removed on the basis of LOAN_NO column. Also any unnecessary columns should be removed. Only columns that should remain in the file are:-
'LOAN_NO', 'UNIT_COD', 'UNITNAME', 'PRODUCT_CODE.x',  'PRODUCT_NAME.x', 'NO_OF_INSTALMENTS', 'ODAMT', 'ODDAYS', 'REGIS_DATE', 'VILLAGE_CODE', 'AGE', 'GENDER', 'CATEGORY_TYPE', 'PIN_CODE', 'ID_NO', 'FAMILY_MEM', 'FAMILY_MEN', 'FAMILY_WOM', 'HOUSE_TYPE', 'ASSET_BASE', 'REGULAR', 'FESTIVE', 'ACTIVE_YN', 'ACCOMADATION', 'APPL_AMOUNT',  'ACTIVITY_CODE', 'ACTIVITY_NAME'

If required, start date and end date can be used to filter out the data for a particular period.
In the code default has been described as when ODDAYS is more than 90.
All categorical variables have been encoded and the numerical variables have been scaled by min max scaling.

The no of clusters formed by the unsupervised learning code can be altered by changing the n_clust parameter which has been currently set to 10. The number of times you want the clustering code to run is controlled by the n_init parameter. The clustering is done  n_init times and the best result based on loss is taken finally.

Location of the centroid is described as particular values of numerical attributes and a value of the categorical attributes. Distance is defined by using Euclidean distance for numerical features and no. of similar categorical features.

The cluster column corresponding to every LOAN NO is appended to the original csv file and stored as cleaned_v2_with_clusters_vs_ID_Adilabad.csv.

Summary statistics for every categorical attribute is done on the basis of each cluster’s composition as well as overall category count.
Mean, Min, Max and  Median for each numerical attribute has been reported within each individual cluster.


 

