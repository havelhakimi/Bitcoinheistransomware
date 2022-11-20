# Decision Trees, Ensembling, Adaboost and Random Forest on  Bitcoin Heist Ransomware Address Dataset
This a solution notebook to an assignment question given in a Data Mining graduate course. Each code block carries is accompanied by  relevant analysis wherever required. </br>
**Dataset link** : https://archive.ics.uci.edu/ml/datasets/BitcoinHeistRansomwareAddressDataset </br>
Broadly, the following steps have been performed in the solution notebook:
<ul>
<li> A custom designed train-test split method which splits the data into training, validation and test set (70:15:15). </li>
<li> Decision Tree trained using both the Gini index and the Entropy by changing the max-depth as [4,8,10,15,20]. </li>
  <ul> <li>The criteria (gini/entropy) selected is the one which gives better accuracy on test set with the chosen depth. </li></ul>
  
<li> Ensembling method is a method to combine multiple not-so-good models to get a better performing model.</li> 
  <ul>
  <li> Created 100 different decision stumps (max-depth 3). For each stump trained it on a randomly selected 50% of the training data i.e. selelct data for each stump separately </li>
  <li> Finally predicted the test samples's labels by taking a majority vote of the output of the stumps. </li>
  
  </ul>

<li> Used the sklearn Adaboost algorithm on the above dataset and reported the testing accuracy. </li>
  
  <ul> 
  <li> Decision tree is used as the base estimator and with a number of estimators as [4,8,10,15,20]. </li>
  <li>Further compared the Random Forest and Adaboost results. </li>
  </ul>
</ul>
These above assumptions and the flow of work is according to the questions asked in assignment.
