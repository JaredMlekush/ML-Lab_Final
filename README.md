# ML-Lab_Final

Link to find at Deepnote: https://deepnote.com/project/ccb00087-ba61-4db1-ba97-3a0ee74eb21a#%2FFinal_notebook.ipynb

Repository includes:
  - "Behind the scenes" look at the process
  - Notebook to profile data
  - Final Notebook
  - The data used
  - Results from the profiling

Found above is the culmination of a data science project- overview below.

Utilizing the public dataset about Pokemon, found here -> https://www.kaggle.com/alopez247/pokemon?select=pokemon_alopez247.csv

I created a Supervised Machine Learning problem. This was done by extracting a numerical column from the data and using it as the target variable. That is, I wanted to see if the other columns of the dataframe (Name, Attack, Speed, Defence, etc.) had "clues" within it that would allow me to predict the "Generation" the Pokemon was from.
Initial results were relatively strong - with the best baseline model being Logistic Regression with: f1_score = accuracy = 0.685
Tested out 3 different classifiers, searching through them and allowing the algorithm to test out different hyperparameters for each model to obtaing the "best" overall model. Logistic Regression remained victorious, giving: f1_score = 0.7925 and accuracy = 0.7979.
Wanting to know if I could squeeze any more out of the model, I applied K-means clustering to the data, which allowed me to bring up my final scores to: f1_score = 0.86575 and accuracy = 0.8457, on the training sets.
This appeared to be quite promising- except when tested on the Test data scores were only slightly better than baseline at f1_score = 0.712 and accuracy = .724

Going forward: Additional clustering techniques (and assessing via their evaluation metrics) may be a feasible and worthwhile option to explore. Additionally, performing some feature importance/PCA might allow for a simplification of the model (though it is not particularly "complex"). Less features allow for better interpretability.
