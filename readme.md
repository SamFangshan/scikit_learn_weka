#WEKA-ScikitLearn Wrapper
##Introduction
This wrapper is able to make a WEKA classifier compatible with a Scikit-Learn classifier, especially when building a VotingClassifier.
##Assumptions
###Only single-label classification is carried out
###Training & Testing data are passed in as either Pandas Data Frames or Numpy Arrays
##Usage Example
```python
from scikit_learn_weka.wrapper import ScikitLearnWekaWrapper
from weka.classifiers import Classifier
cls = Classifier(classname="weka.classifiers.functions.SMO", options=["-N", "0"])
cls = ScikitLearnWekaWrapper(cls)
cls.fit(X, y)
print(cls.score(X_test, y_test))
```
