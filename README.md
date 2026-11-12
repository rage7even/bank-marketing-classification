# Bank Marketing Classification

This KBTU Introduction to Machine Learning team project compares three classifiers for predicting term deposit subscriptions. It uses the public UCI Bank Marketing dataset of 45,211 records. About 12% of records are positive, so we evaluated precision, recall and F1 for the subscription class.

## Run the notebook

Use Python 3.11 or 3.12 in a virtual environment. The notebook downloads its input from UCI, so running it requires an internet connection.

~~~sh
python -m pip install -r requirements.txt
python -m notebook bank_marketing.ipynb
~~~

Select **Run All Cells** to repeat the exploratory analysis, preprocessing and model comparison. The notebook includes the exploratory analysis and modelling in one file. The saved results below come from the original coursework run.

| Model | Test precision | Test recall | Test F1 | Mean 5-fold CV F1 |
| --- | ---: | ---: | ---: | ---: |
| Logistic regression | 0.67 | 0.36 | 0.47 | 0.4623 |
| 5-nearest neighbours | 0.61 | 0.32 | 0.42 | 0.3829 |
| Decision tree, depth 5 | 0.64 | 0.32 | 0.43 | 0.4513 |

## Evaluation limits

The coursework uses call duration, which becomes available after the call. For pre-call targeting, remove duration and log_duration and evaluate the models again. The coursework also encodes categories and fills missing values before splitting the data. Its cross-validation uses scaling fitted on the full training split. A stricter evaluation would fit all learned preprocessing inside a scikit-learn pipeline within each fold and recompute the metrics.

## Team and contribution

Machine Learners team at Kazakh-British Technical University. Myktybek Aksungkar, Yerkinbek Oren, Gazhbek Aruzhan and Aushet Askhat.

Yerkinbek Oren led exploratory data analysis and preprocessing, implemented six visualizations, and prepared the features and stratified train/test split for the team's model comparison.

[Dataset source and citation](https://archive.ics.uci.edu/dataset/222/bank+marketing)
