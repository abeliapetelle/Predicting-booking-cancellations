# Predicting-booking-cancellations

## Objective
Clustering booking clients and predicting booking cancellations using supervised and unsupervised machine learning algorithms.

## Data
This data set contains a single file which compares various booking information between two hotels: a city hotel and a resort hotel. Both hotels are located in Portugal (southern Europe). The data contains "bookings due to arrive between the 1st of July of 2015 and the 31st of August 2017".
The shape of the dataset : 119368 rows, 32 columns. 

## Context
Today, many hotels are trying to categorize their customers such as their needs, wants, characteristics in order to approach them in the most effective way.
In data analysis, this can be possible by clustering clients with unsupervised machine learning algorithms.

Another challenge for hotels is to be able to identify in advance customers who are going to cancel their reservation. By knowing this information, they can better plan personel and food requirements for instance.

## Process
- Data cleaning
- Exploratory data analysis
- Unsupervised learning - clustering booking clients
- Supervised learning - predicting cancellations

## Result of the clustering with UMAP visualization 
<img src="https://github.com/abeliapetelle/Predicting-Booking-Cancellations/blob/master/Media/Clustering%20with%20UMAP%20visualization.png" width="40%" height="40%">

The silhouette score is at 0.48 and Davies Bouldin score at 1.3. 
Even if these metrics are not bad, visually, we do not see clear separations between clusters. 
It is often difficult to see the result of a clustering in a two dimensions visualisation. But as I used the PCA method, we cannot visualize the result in three dimensions. The best is to see the impact of these clusters in the modeling part. 

## Objective & Result of the classification models 
<img src="https://github.com/abeliapetelle/Predicting-Booking-Cancellations/blob/master/Media/Objective%20for%20modeling.png" width="60%" height="60%">
The worst case for our client is the risk of over-booking. The main objective of this project was then to reduce the False Positive errors. As a result, the metric to look at was the precision score. 
<br>
<img src="https://github.com/abeliapetelle/Predicting-Booking-Cancellations/blob/master/Media/Model%20comparison%20v2.png" width="60%" height="60%">
The best model regarding the scores is the Random Forest. Since we know that Random forest tends to overfit, we will keep the 'Ensemble' (Voting Classifier) as our final model.

## Conclusion 
- With the Voting Classifier model, we are able to predict a booking cancellation by 86%
- While we weren't confident about our clusters, it turns out to be the 4th most important feature for predicting a cancellation
- Feature that are most important in our model are the following:
<img src="https://github.com/abeliapetelle/Predicting-Booking-Cancellations/blob/master/Media/Most%20important%20features.png" width="50%" height="50%">


## Impovments
- Building a more universal model getting more data from various hotels
- Building a more specialized model with better results focusing only on a specific hotel

## Built With
* [Python](https://docs.python.org/3/) - The programming language used
* [Pandas](https://pandas.pydata.org/pandas-docs/stable/index.html) - library providing high-performance, easy-to-use data structures and data analysis tools for the Python programming language
* [MatPlotLib](https://matplotlib.org/contents.html) - Matplotlib is a Python 2D plotting library which produces publication quality figures in a variety of hardcopy formats and interactive environments across platforms
* [Sklearn](https://scikit-learn.org/stable/) - Sklearn is a machine learning library featuring various classification, regression and clustering algorithms including support vector machines, random forests, gradient boosting and k-means.
* [Seaborn](https://seaborn.pydata.org/index.html) - Seaborn is a Python data visualization library based on matplotlib. It provides a high-level interface for drawing attractive and informative statistical graphics.
* [NumPy](https://numpy.org/) - NumPy is a library adding support for large, multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays. 
* [SciPy](https://www.scipy.org/) - SciPy is an ecosystem of open-source software for mathematics, science, and engineering.
