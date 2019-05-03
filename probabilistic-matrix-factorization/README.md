# Probabilistic Matrix Factorization

Start with matrix $A$ of users' preferences: users are represented by rows, and the items by columns.
Thus, user $i$'s preference for item $j$ is found at $A_{i, j}$.
This matrix can be represented as a  the product of two matrices; one that characterizes the users $U$, and one that characterizes the items $O$ (as in _O_bjects).
These two matrices are the _factors_ of the matrix of user preferences.

These two factor matrices represent the users and items quantitatively.
A single user or item is characterized by a vector.
The size of these vectors is $k$ (ensuring their product is a square matrix).
The value for $k$ is the latent dimensionality, or embedding size, of the factors.
Larger values of $k$ can be used to represent more complex relations; however, this can also lead to overfitting.
The way that this works is somewhat subtle, until you consider the mechanics.

Considering the value at $i, j$ in the user-item matrix $A$.
This value is found by computing the inner-product of user's $i$'s vector from the left matrix $U$, and item $j$'s vector from the right matrix $O$.
Therefore, every user-rating of an item in $A$ is the inner-product of the corresponding rows in $U$ and $O$.
Using common machine learning methods, a model can be trained to produce a representation of user preferences that approximates $A$.  
