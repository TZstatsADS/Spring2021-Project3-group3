# Project: Can you recognize the emotion from an image of a face? 
<img src="figs/CE.jpg" alt="Compound Emotions" width="500"/>
(Image source: https://www.pnas.org/content/111/15/E1454)

### [Full Project Description](doc/project3_desc.md)

Term: Spring 2021

+ Team #3
+ Team members
	+ Maslova, Olha
	+ Li, Qiao
	+ Morrissey, Mark
	+ Yang, Yutong
	+ Zhang, Renyin

+ Project summary: In this project, we created a binary classification engine for facial emotion recognition to differentiate simple emotions (label 1) from complex (label 0). We built several classifiers including GBM, SVC, Linear Regression, KNN, Random Forest, XGBoost, CNN, and Densely connected Neural Network. Given that the dataset was imbalanced we tried diffierent techniques to reduce model overfitting: 
	+ SMOTE undersampling and oversample;
	+ Regularizations in Dense Neural Networks;
	+ Droupout and BatchNormalization layers in both CNN and Neural Networks;
Our dataprocessing included generating features from the given fiducial points and reducing the image size for CNNs.

For our Baseline model - GBM - we got the following results:

	Data Used: fiducial points

	Accuracy: 0.86
	AUC: 0.94
	Training time: 344.22 seconds
	Testing time: 0.00006 seconds per point

For our Advanced model - Weighted SVC - we got the following results:

	Data Used: fiducial points

	Accuracy: 0.863
	AUC: 0.9465
	Training time: 62.867 seconds
	Testing time: 0.007 seconds per point
	
**Contribution statement**: ([default](doc/a_note_on_contributions.md)) All team members contributed equally in all stages of this project. All team members approve our work presented in this GitHub repository including this contributions statement. 

**Note: models in bold were a focus of the contributor**

+ Maslova, Olha: managed communications; pre-processed data for Neural Networks; implemented GBM, **CNN on raw image data, and Neural Network on combined image and fiducial points data**. Contributed to presenatation, organization of Github files, Github ReadMes, and main.ipynb. Tested main.ipynb.

+ Li, Qiao: pre-processed fiducial points data; implemented **Weighted SVMs (fine-tuned)**, KNeighborsClassifier (slightly fine-tuned), DecisionTreeClassifier (not fine-tuned), RandomForestClassifier(not fine-tuned), AdaBoostClassifier (not fine-tuned); Contributed to presenatation, organization of main.ipynb and all other Github files, Github ReadMes, test script

+ Morrissey, Mark: implemented XGBoost, Ridge Classifier, Adaboost, and **Voting classifier (fine-tuned)**; Fine-tuned logistic regression and an alternative SVM for use in the final Voting Classifier model. Explored PCA and recursive feature elimination for dimensionality reduction reduction (did not improve error rate). Contributed to presenatation, Github ReadMes.

+ Yang, Yutong: performed initial model trials (SVC, KNN, SGD, RandomForest, Adaboost, XGBoost). Fine-tuned GBM on on fiducial points. Implemented **CNN** on raw images; Contributed to presenatation, organization of main.ipynb, all other Github files, Github ReadMes. Re-run all the models to time.

+ Zhang, Renyin: Researched possible models and fine tuned the models that teammates created, focusing on cnn and AdaBoost with SVM.

**In order to start**: Follow the link download then install python and Anaconda.
https://docs.anaconda.com/anaconda/install/

**Sources:**
- Hands-On Machine Learning with Scikit-Learn & TensorFlow,  Aurelien Geron
- Deep Learning with Python, Francois Chollet
- https://www.tensorflow.org/tutorials/images/classification
- https://www.tensorflow.org/tutorials/structured_data/imbalanced_data
- https://www.mathworks.com/help/vision/ref/triangulate.html


Following [suggestions](http://nicercode.github.io/blog/2013-04-05-projects/) by [RICH FITZJOHN](http://nicercode.github.io/about/#Team) (@richfitz). This folder is orgarnized as follows.

```
proj/
├── lib/
├── data/
├── doc/
├── figs/
└── output/
```

Please see each subfolder for a README file.
