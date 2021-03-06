K-Means
===  
example1             |  example2
:-------------------------:|:-------------------------:
![](https://github.com/yja938882/K-Means/blob/master/example/example1.png)  |  ![](https://github.com/yja938882/K-Means/blob/master/example/example2.png)

https://yja938882.github.io/d3_practice/k_means.html

Load
=== 
> ```javascript
> <script type="text/javascript" src="/* path */k_means.js"></script>
  
DataFormat
=== 
> ```javascript
> var Data = [
>  [0.5, 0.7],
>  [3.6, 0.11],
>  ...
> ];
>```

 
Docs
===
#### &nbsp;&nbsp;Constructor  

</br>

* **K_Means(args)**   

> ```javascript
> var kmeans = K_Means( { k : 3, data : [[0.5], [0.6], ... ] });
> ```
> * ```args``` Object 
>    *  ```k``` Number : # of clusters.
>    *  ```data``` Array : Array of data points.  

</br></br>

#### &nbsp;&nbsp; Methods 

</br>

* **clustering(dist, callback1, callback2, callback3)**

> ```javascript
> /* Clustring. */
> kmeans.clustering(kmeans.euclidean, render1, render2, render3);
> ```
> * ```dist``` Function : Distance function.
> * ```callback1``` Function : Function that is called after Assignment Step.
> * ```callback2``` Function : Function that is called after Update Step.
> * ```callback3``` Function : Function that is called after clustering.

</br></br>

* **setNearestCluster(dist, callback)**

> ```javascript
> /* Assignment Step. Assign each observation to the cluster. */
> kmeans.setNearsetCluster(kmeans.euclidean, render);
> ```
> * ```dist``` Function : Distance function.
> * ```callback``` Function : Function that is called after Update Step.

</br></br>
  
* **updateCentroid(callback)** 

> ```javascript
>/* Update Step. Calculate the new means to be the centroids */
> kmeans.updateCentroid(render);
> ```
> * ```callback``` Function : Function that is called after Update Step.

</br></br>
  
* **euclidean(pointA, pointB)** 

> ```javascript
> /* Euclidean distance function. */
> var dist = kmeans.euclidean(pointA, pointB);
> ```
> * ```pointA``` Array\<Number\> : point.
> * ```pointB``` Array\<Number\> : point.

</br></br>

* **manhattan(pointA, pointB)** 

> ```javascript
> /* Manhattan distance function. */
> var dist = kmeans.manhattan( pointA, pointB);
> ```
> * ```pointA``` Array\<Number\> : point.
> * ```pointB``` Array\<Number\> : point.

