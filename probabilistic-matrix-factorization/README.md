# Probabilistic Matrix Factorization

Start with a matrix of users' preferences: users are represented by rows, and the items by columns.
Thus, user $i$'s preference for item $j$ is found at the index $i, j$.
This matrix can be represented as a  the product of two matrices; one that characterizes the users, and one that characterizes the items.
These two matrices are the _factors_ of the matrix of user preferences.

These two factor matrices represent the users and items quantitatively.
Each row vector in the matrices represent a single user or item, and the column vectors represent certain features that are used to characterize the corresponding user or item.
The size of the column space for both matrices is $k$ (ensuring their product is a square matrix).
The value for $k$ is the latent dimensionality, or embedding size, of the factors.
Larger values of $k$ can be used to represent more complex relations; however, this can also lead to overfitting.
