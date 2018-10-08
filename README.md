# Project: Creating Customer Segments
## Category: Unsupervised Learning

### Overview

In this project, I analyzed a dataset that contains various customers' annual spending amounts corresponding to product categories. The goal of this project is to identify customer segments hidden in this dataset.

I first explored the data by selecting a small subset to sample and determine if any product categories highly correlate with one another. Afterwards, I preprocessed the data by scaling each product category and then identifying (and removing) unwanted outliers. With the good, clean customer spending data, I applied PCA transformations to the data and implement clustering algorithms to segment the transformed customer data.
I researched and compared two algorithms, K-Means clustering and Gaussian Mixture Model clustering, then I chose the Gaussian Mixture Model for my clustering.
Finally, I compared the segmentation found with an additional labeling and considered ways this information could assist the wholesale distributor with future service changes.

### Setting

A wholesale distributor recently tested a change to their delivery method for some customers, by moving from a morning delivery service five days a week to a cheaper evening delivery service three days a week. Initial testing did not discover any significant unsatisfactory results, so they implemented the cheaper option for all customers. Almost immediately, the distributor began getting complaints about the delivery service change and customers were canceling deliveries, losing the distributor more money than what was being saved.

My goal is to find out what types of customers they have to help them make better, more informed business decisions in the future. By using unsupervised learning techniques, I will see if any similarities exist
between customers, and how to best segment customers into distinct categories.

### Techniques

- preprocessing techniques such as feature scaling and outlier detection
  - visualizing the distribution by scatterplots
  - visualizing the correlation between features by a heatmap
  - applying logarithmic scaling
  - Tukey's Method for identifying outliers
- interpreting data points that have been scaled, transformed, or reduced from PCA
- analyzing PCA dimensions and constructing a new feature space
- data clustering using unspervised learning techniques
  - K-Means clustering
  - Gaussian Mixture Model clustering
  - silhouette score
- assessment and use of the clustering
  - A/B test


### Libraries

This project requires **Python 2.7** and the following Python libraries installed:

- [NumPy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org)
- [matplotlib](http://matplotlib.org/)
- [scikit-learn](http://scikit-learn.org/stable/)

This project runs on a [Jupyter Notebook](http://ipython.org/notebook.html)

### Files

- `customer_segments.ipynb` (Jupyter notebook, This project's main file)
- `visuals.py` (Python, visualization functions)
- `customers.csv` (dataset file)

### Data

The customer segments data is included as a selection of 440 data points collected on data found from clients of a wholesale distributor in Lisbon, Portugal. More information can be found on the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Wholesale+customers).

Note (m.u.) is shorthand for *monetary units*.

**Features**

 1. `Fresh`: annual spending (m.u.) on fresh products (Continuous);
 2. `Milk`: annual spending (m.u.) on milk products (Continuous);
 3. `Grocery`: annual spending (m.u.) on grocery products (Continuous);
 4. `Frozen`: annual spending (m.u.) on frozen products (Continuous);
 5. `Detergents_Paper`: annual spending (m.u.) on detergents and paper products (Continuous);
 6. `Delicatessen`: annual spending (m.u.) on and delicatessen products (Continuous);
 7. `Channel`: {Hotel/Restaurant/Cafe - 1, Retail - 2} (Nominal)
 8. `Region`: {Lisbon - 1, Oporto - 2, or Other - 3} (Nominal)
