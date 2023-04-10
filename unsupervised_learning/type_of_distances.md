### CONTENT
#### Different distance measures used by machine learning algorithms:
- Euclidean Distance
- Manhattan Distance
- Cosine Similarity
- Hamming Distance
- Minkowski Distance

In all the distances explained below $x_{1}$ and $x_{2}$ points are considered as vectors of dimension
**d**

#### Euclidean Distance:
<img src = https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/015/423/original/Screenshot_2022-09-30_at_3.32.07_PM.png?1664532217 height = 400 width = 400>

- It's the most commonly used distance measure.
- It can be defined as the length of segment joining two points.

- The formula of Euclidean distance for two points of dimensionality d is:   
> - Euclidean $(x_1,x_2) = ( ∑_{j=1}^{j=d} {{ (x _{1j} - x _{2j} )}^2) }^{\frac{1}{2}} $

- The formula is simply using pythagorean theorem on the cartesian coordinates to calculate the distance.

**Properties**
- It is very intuitive to use.
- It is not scale invariant (One has to normalize the data before using this)
- As the dimensionality of data increases, this becomes lesser useful due to curse of dimensionality.



#### Manhattan Distance:
<img src = https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/015/438/original/Screenshot_2022-09-30_at_5.36.14_PM.png?1664538989 height = 400 width = 400>

- Its also called taxi-cab or city-block distance
- Imagine vectors that describe objects on a uniform grid such as a chessboard.Now Manhattan distance refers to the distance between vectors if they can move right or left only. There is no diagonal moment involved while calculating this distance.
- Manhattan $(x_1,x_2) = ∑_{j=1}^{j=d} {{ | x _{1j} - x _{2j} |} } $
- When the data has discrete or binary attributes, manhattan distance is helpful because it takes only those values into account which are possible.


#### Cosine Similarity
<img src = https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/015/440/original/Screenshot_2022-09-30_at_5.48.27_PM.png?1664539782 height = 400 width = 400>

- Cosine Similarity is used to counteract the high dimensionality problem of euclidean distance
- The cosine similarity is simply the cosine of the angle between two vectors. It is the inner product of the vectors if they were normalized to both have length one.
- $D(x_{1}, x_{2})$ = $\cos (\theta ) =   \dfrac {x_{1} \cdot x_{2}} {\left\| x_{2}\right\| \left\| x_{2}\right\|} $
- It is used in high dimensional data
- It is very commonly used in text-analysis related tasks.
- Cosine similarity doesn't take magnitude of vectors into account, just their direction is considered.


#### Hamming Distance:
<img src=https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/015/442/original/Screenshot_2022-09-30_at_6.36.29_PM.png?1664542613 height = 400 width = 400>

- It is calculated as the number of positions at which the values of coordinates are different in two vectors. For eg. in the image shown above its simply 2.
- It is typically used to compare binary strings
- It can also be used to calculate similarity of strings
- It is difficult to use when two vectors are of different lengths
- It doesn't take actual values into account
- It is not usable when magnitude is important
- It is used in error correction/detection when transferring data
- It can be used to measure the distance between categorical variables


#### Minkowski Distance:
<img src=https://d2beiqkhq929f0.cloudfront.net/public_assets/assets/000/015/443/original/Screenshot_2022-09-30_at_6.50.24_PM.png?1664543477 height = 400 width = 400>

- It is a distance used in normed vector space, i.e. in a space where distances can be represented as vectors.
- It is actually generalization of euclidean and manhattan distances.
- Minkowski$(x_1,x_2) = ( ∑_{j=1}^{j=d} {{ (x _{1j} - x _{2j} )}^p) }^{\frac{1}{p}} $, where p can be used to manipulate the distance metric.
- Here if p=1 => Manhattan distance.
- Here if p=2 => Euclidean distance.
- Here if p=infinity => The distance will become the greatest of difference between two vectors along any coordinate dimension.
- We can iterate over different values of p to get a distance which works best for our use case.