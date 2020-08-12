# stock clustering

***
in this exercise we want to cluster stocks of 500 large companies traded in the American market <br>
from 10/5/2019 to 11/5/2020 and see how companies affected during the coronavirus period. <br>
we got the symbols of the largest companies in the United States from [S&P 500](https://www.slickcharts.com/sp500),
and the data from Yahoo Finance DataReader : 

example : to get Microsoft data : 
```python
start = datetime(2019,5,10)
end = datetime (2020,5,11)
data = web.DataReader("MSFT",'yahoo',start,end)
```

print the data : <br><br>
<img width="414" alt="a" src="https://user-images.githubusercontent.com/69496372/89972074-95210c00-dc65-11ea-9001-92e78d534ae2.png">

<br><br>
## in this exercise we will use : 
* Kmeans Clustring
* Silhouette score : metric used to calculate the goodness of a clustering technique
* The Elbow method : to choose best k (clusters)
* Hierarchical - Agglomerative Clustering with single,complete,average and ward methods.
* dendrogram to find the optimal k
* Gaussian Mixture Model
* PCA technique , before and after clustering . 

***
### Hierarchical Clustering , ward method : dendrogram<br>
<img width="1020" height="300" src="https://user-images.githubusercontent.com/69496372/89972526-bcc4a400-dc66-11ea-9e83-530ca7fcffe8.png">

### daily return average for the two clusters : we see how the companies in red cluster affeced during the coronavirus period <br>
<img width="950" height="300" src="https://user-images.githubusercontent.com/69496372/89972537-c1895800-dc66-11ea-9a70-fdec1e5aa821.png">


### PCA of 50 companies  : PCA **before** clustering:
<img width="500" height="250" src="https://user-images.githubusercontent.com/69496372/89972534-bfbf9480-dc66-11ea-9b87-989a69011b45.png">


### PCA of 50 companies  : PCA **after** clustering:
<img width="500" height="250" src="https://user-images.githubusercontent.com/69496372/89972530-be8e6780-dc66-11ea-98e9-e7a93cacc79f.png">
