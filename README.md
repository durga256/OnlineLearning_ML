# OnlineLearning_ML
This analysis is from data presented in the research paper: <a href="https://drive.google.com/file/d/1NusaE6mBEhDd4vosOzGJsJKc2nNoaJ7Y/view?usp=sharing">Challenges in benchmarking stream learning algorithms with real-world data</a>

This project analyses a streaming dataset of insects. The Machine Learning algorithm then decides if it is a pest or not. Classification algorithms applied include:
<ul>
  <li>No-change Classifier</li>
  <li>Majority Class Classifier</li>
  <li>Hoeffding Trees</li>
  <li>SAM-KNN</li>
  <li>Hoeffding Adaptive Trees(HAT)</li>
  <li>Adaptive Random Forest(ARF)</li>
  <li>Leverage bagging</li>
</ul>
The dataset is seperated based on the kind of drifts the dataset showcases. The above algorithms are applied to the datasets with 3 different drift patterns(Incremental, Abrupt and Gradual)
The accuracies of the above algorithms on Incremental dataset is shown below
<p align="center"><img src="https://drive.google.com/uc?export=view&id=1Z0hduh-r-OxRqtg7EKJ5mGNPuPePKHCb" alt="PerformanceGraphIncrementalDataset"></p>
As expected the No-change classifier and Majority Class Classifier being very basic ones deliver poor performance. The ARF delivers the best performance on this dataset
Similarly, The accuracies of the above algorithms on Gradual dataset is shown below
<p align="center"><img src="https://drive.google.com/uc?export=view&id=1f5TKAYWq4D-0tI9pGEsTQv1napDA0eML" alt="PerformanceGraphGradualDataset"></p>
A similar trend is followed except the No-Change and Majority classifiers peak for a period of time. This could be due to the fact the data remains constant for a certain period of time resulting in no-change in the result and the majority of the resulting classes are same. However, over time we observe that Leverage Bagging performs the best predictions.
Also, The accuracies of the above algorithms on abrupt dataset is shown below
<p align="center"><img src="https://drive.google.com/uc?export=view&id=1MDy5SZdW-ah0XXFIP2Xa0r3qpE5afp4i" alt="PerformanceGraphAbruptDataset"></p>
A similar trend is followed except the No-Change and Majority classifiers peak for a period of time. This could be due to the fact the data remains constant for a certain period of time resulting in no-change in the result and the majority of the resulting classes are same.
<br />However, over time we observe that Leverage Bagging performs the best predictions.
<br />ADWIN is used as drift detection method to accomodate for changes over seasons(different insects populate over different seasons)
<br />The ADWIN drift detection algorithm does not detect any drifts in the incremental dataset. The occurence of drifts for the Gradual and Abrupt dataset has been visualised below:
<p align="center"><img src="https://drive.google.com/uc?export=view&id=1lRUvvTOHgC5QBqQL60kHnMGrIIBnIqpD" alt="DriftsInGradualDataset"></p>
<p align="center"><img src="https://drive.google.com/uc?export=view&id=1klA4bQzoka7HwhfCpoI4UgOx4OFXP-0u" alt="DriftInAbruptDataset"></p>
The final accuracies of different algorithms on different dataset is shown below
<p align="center"><img src="https://drive.google.com/uc?export=view&id=11iXLib2u-X9JVS1qnWh3mnBDRXbsqDKe" alt="FinalAccuraciesOfAllAlgorithms"></p>
