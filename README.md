# Classification-Techniques-Expirament
Analyzing multiple classification Techniques as Logistic Regression, KNN, LDA, SVM,
Decision Tree, Random Forest, XGBOOST and ADABOOST. I compared their performance
based on misclassification rate and weighted cost functions.

The "breast-cancer-wisconsin.csv" dataset contains 9 attributes and a
binary response variable, which is an indicator for breast cancer, for each of the
683 patients. The first column in the data holds the patients' ID numbers, which is
not considered as an attribute. The last column holds the response variable, which
takes the values 2 for healthy and 4 for sick. I normalized it to 0 and 1,
respectively. The remaining 9 columns are used as the attributes. Since the scale is
the same for all attributes, we didn't need to normalize them. We also used the first 
400 instances as the training set, and the remaining ones as the test set.

At the end we compared the classification algorithms in the previous parts in terms
of misclassification rate and the following weighted cost; 

c = (1/6916) sum[i=1:283](ci)

where ci is the cost of the decision for instance i in the test set. 283 is
the total number of test instances, and 6916 is the maximum cost when all
instances are misclassified with respect to the following decision costs. 
zero cost is used for correctly classified instances, and cost 1 for healthy 
instance misclassified as sick, and cost 100 for sick instance misclassified
as healthy. Since there are 216 healthy and 67 sick instances in the test set,
the maximum cost is 67 x 100 + 216 = 6916 if all instance were classified
as healthy.
