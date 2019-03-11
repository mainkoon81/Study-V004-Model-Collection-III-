# Non-Parametric Models
<img src="https://user-images.githubusercontent.com/31917400/54094265-9a569900-4397-11e9-9606-5c31b30cb7a6.jpg" />

> **Parametric Models**
 - It has a fixed number of parameters and makes **stronger assumptions** about the data, so it works well if the assumptions turn out to be correct, but it may perform badly if the assumptions are wrong.
 - It is computationally faster.
> **Non-Parametric Models**
 - It uses a flexible number of parameters, and the number of parameters often grows as it learns from more data.
 - It makes fewer assumptions about the data and does not make any assumptions on the underlying data distribution, so can be the first choices for a classification study when there is little or no prior knowledge about the distribution of data. 
   - "Let the data speak for itself."
 - It is computationally slower.

## 1> K-Nearest Neighbor Methods
> keywords: K, distance, ties, NaN, **K-D_Trees**(booster)
 - KNN can be used for **classification**: 
   - the output is a class membership(predicts a class or a discrete value). An object is classified by a majority vote of its K nearest neighbors, with the object being assigned to the class most common among them. 
 - KNN can be used for **regression**:
   - the output is the value for the object(predicts continuous values). This value is the **average(or median)** of the values of its k nearest neighbors.
   
 - Let's say we have a new data pt to classify. And we are going to use "K" other neighbor data pts around the protagonist data pt. Then vote. Which neighbor data pts would claim this protagonist data pt? 
 - Voronoi tesselation(partitioning space into regions)
   - its decision surf is non-linear and reflects labels very well.  
   - This is very sensitive to outliers. A single, mislabeled data pt can dramatically change the boundary, thus we need to consider multiple neighbors(K) to make decision!
 <img src="https://user-images.githubusercontent.com/31917400/54119361-0d3e2f00-43ed-11e9-9997-7b02d2f72e3b.jpg" />

 - (+)
   - One of the great things about KNN is that we can add in new data to update the model very easily!
   - VOTING(for classification) is damn easy. AVG(for regression) is damn easy
 - (-)
   - Too sensitive to irrelevant features(outliers or mislabeled) and the scale of the data
   - No missing data allowed. All points are considered. 
   - Expensive computation. Need to store all training data points. Need to compute distance to all other points.   

### a) Classification
<img src="https://user-images.githubusercontent.com/31917400/54120609-09f87280-43f0-11e9-821c-7eb0eadf0812.jpg" />




### b) Regression





### How to improve speed? 
__[KD tree]:__ 




































