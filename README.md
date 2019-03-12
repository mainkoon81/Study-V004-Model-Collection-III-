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
Let's say we have a new data pt to classify. And we are going to use "K" other neighbor data pts around the protagonist data pt. Then vote. Which neighbor data pts would claim this protagonist data pt? Ask you neighbors.

> What for?
 - KNN can be used for **classification**: 
   - the output is a class membership(predicts a class or a discrete value). An object is classified by a majority vote of its K nearest neighbors, with the object being assigned to the class most common among them. 
 - KNN can be used for **regression**:
   - the output is the value for the object(predicts continuous values). This value is the **average(or median)** of the values of its k nearest neighbors.

> What to know?
 - **Normalization** techniques should almost always be applied when nearest neighbor models are used. 
 - **Feature selection** is a particularly important process for KNN as it alleviates the curse of dimensionality.
   - curse of dimensionality: as dimensionality increases, the size of data points we need grows exponentially. So every time we add features, we need crazy more data: `original_size^dim`
 - **Voronoi tesselation**, partitioning space into regions: **(K=1)NN**
   - its decision surf is non-linear and reflects labels very well.  
   - This is very sensitive to outliers. A single, mislabeled data pt can dramatically change the boundary, thus we need to consider "bigger K" to make decision!
 <img src="https://user-images.githubusercontent.com/31917400/54119361-0d3e2f00-43ed-11e9-9997-7b02d2f72e3b.jpg" />

 - **Choosing k**
   - Affecting smoothness of decision surf, and its output as well. 
   - If K is too small:
     - gives inconsistent output due to high variability
   - If K is too large:
     - gives unnecessarily stable prior probability coz it considers whole datapoint and always bigger size(the most probable) class will win.
   - Then how to pick K?
     - Cross-validation 
     
 - **Distance measure**
   <img src="https://user-images.githubusercontent.com/31917400/54166587-ce948d00-445d-11e9-8dc9-e379be3ec781.jpg" />
   - Which point is closer?
   - **Euclidean** for numeric attributes: treat all dimensions equally
   - **Hamming** for categoric attributes: gives how many matches..(match:1 / unmatch:0)
   - **Minkowski**(generalized Euclidean): Based on **P**, output varies, and it changes geometry of space.  
 
 - **Weighted KNN**
   - Some inputs are more relevant than others. How to? 
   
 
 - **(+)** of KNN
   - Add in new data to update the model very easily!
   - VOTING(for classification) is damn easy. AVG(for regression) is damn easy
   - Works well with both categorical and numerical data
 - **(-)** of KNN
   - Too sensitive to irrelevant features(outliers or mislabeled) and the scale of the data
   - Unlike Decision tree or NaiveBayes, No missing data allowed because all points are considered. 
   - Expensive computation. Need to store all training data points. Need to compute distance to all other points.   

 - **Other Issues**
   - What if..the same number of votes from different classes?
     - In binary case, this can often happen when K is even number. Odd doesn't work when it comes to multiclass classification. 
     - `Breaking ties:`
       - Pick class with **greater prior**(most probable)
       - Use K=1..Voronoi tesselation
   - What if..NaN ?
     - Needed to fill in !!! intolerable !!! Use AVG...

### a) Classification
<img src="https://user-images.githubusercontent.com/31917400/54120609-09f87280-43f0-11e9-821c-7eb0eadf0812.jpg" />

### b) Regression
<img src="https://user-images.githubusercontent.com/31917400/54137775-2ad3be80-4416-11e9-87c3-f91dee1760b1.jpg" />

### c) How to improve speed? 
__[KD tree]:__ 




































