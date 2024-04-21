The main objective of the project is to make a recomendation system where the user inputs a movie
and the output is a series of similar films

The development will take place using docker containers to improve deployment

## Model:

The model will be based of a factorized matrix in order to compare the likings of diferent ussers in order
to know what to recommend.

The matrix will be compose of rows representing the users and columns representing the movies, the values will represent what a user thinks of a movie
x(ij) is what a user i thinks of the movie j. This matrix can get very large and most values will be empty since most users only rate a small set of movies.

- $N$ is the number of users,
- $M$ is the number of movies,
- $A_{ij}$ is the rating of the $j$th movies by the $i$th user,
- each row $U_i$ is a $d$-dimensional vector (embedding) representing user $i$,
- each row $V_j$ is a $d$-dimensional vector (embedding) representing movie $j$,
- the prediction of the model for the $(i, j)$ pair is the dot product $\langle U_i, V_j \rangle$.
