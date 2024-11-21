# Assignment 3

In this assignment, you will complete a number of Numpy and Matplotlib exercises.  You must use the Numpy and Matplotlib libraries to complete the assignment, no `for` loops are allowed, you may not use `Pandas` or any other libraries. 

Please accept the [GitHub Classroom assignment](https://classroom.github.com/a/c1ts9NYG) and clone the repository to get started.

## Exercise 1 (20 pts)

Create a function that takes two parameters, say $(A)$ and $(B)$, and returns the result of their matrix multiplication as a NumPy array, say $(C)$. The function should compute the product $(C = A \times B)$ where $(A)$ is an $( m \times n )$ matrix and $( B)$ is an $(n \times p)$ matrix. The resulting matrix $(C)$ should have shape $(m \times p)$.

The file, `exercise1.py`, contains a function signature with docstring and doctests. Make sure to test your implementation by running the doctests.

```
python -m doctest -v exercise1.py
```

_hint: My solution adds 4 lines of code to the function signature provided in the file._

## Exercise 2 (20 pts)

Create a function that takes four parameters, say $( n )$, $( a )$, $( b )$, and $( c )$, and returns an $( n \times n )$ NumPy array, say $( M )$, such that the diagonal entries of $( M )$ are all equal to $( a )$, the entries of $( M )$ above the diagonal are equal to $( b )$, and the entries of $( M )$ below the diagonal are equal to $( c )$. For example, a call to your function with the arguments $( n = 7 )$, $( a = 3 )$, $( b = 4 )$, and $( c = -8 )$ would return the array:

$$
\begin{bmatrix}
3 & 4 & 4 & 4 & 4 & 4 & 4 \\
-8 & 3 & 4 & 4 & 4 & 4 & 4 \\
-8 & -8 & 3 & 4 & 4 & 4 & 4 \\
-8 & -8 & -8 & 3 & 4 & 4 & 4 \\
-8 & -8 & -8 & -8 & 3 & 4 & 4 \\
-8 & -8 & -8 & -8 & -8 & 3 & 4 \\
-8 & -8 & -8 & -8 & -8 & -8 & 3 \\
\end{bmatrix}
$$

The file, `exercise2.py`, contains a function signature with docstring and doctests. Make sure to test your implementation by running the doctests.

```
python -m doctest -v exercise2.py
```

_hint: My solution adds 5 lines of code to the function signature provided in the file._  

## Exercise 3 (20 pts)

Write a function that takes as a parameter a NumPy array (which could be 1-D or 2-D) and returns the number of entries in the input array that are negative.  For example, if the input array is:

$$
\begin{bmatrix}
3 & 4 & 4 & 4 \\
-8 & 3 & 4 & 4 \\
-8 & -8 & 3 & 4 \\
-8 & -8 & -8 & 3 \\
\end{bmatrix}
$$

then the function should return 6, since there are six negative entries in the array.

The file, `exercise3.py`, contains a function signature with docstring and doctests. Make sure to test your implementation by running the doctests.

```
python -m doctest -v exercise3.py
```

_hint: My solution adds 1 line of code to the function signature provided in the file._

## Exercise 4 (20 pts)

Write a function that accepts a single Numpy array as input. Make a copy of the array, then use fancy indexing to set all negative entries of the copy to 0. Return the resulting array.  For example, if the input array is:

$$
\begin{bmatrix}
3 & 4 & 4 & 4 \\
-8 & 3 & 4 & 4 \\
-8 & -8 & 3 & 4 \\
-8 & -8 & -8 & 3 \\
\end{bmatrix}
$$

then the function should return:

$$
\begin{bmatrix}
3 & 4 & 4 & 4 \\
0 & 3 & 4 & 4 \\
0 & 0 & 3 & 4 \\
0 & 0 & 0 & 3 \\
\end{bmatrix}
$$

The file, `exercise4.py`, contains a function signature with docstring and doctests. Make sure to test your implementation!

```
python -m doctest -v exercise4.py
```

_hint: My solution adds 3 lines of code to the function signature provided in the file._

## Exercise 5 (20 pts)

In your Physics class, you have been studying the free fall of objects.  You have learned that the height of an object in free fall is given by the equation:

$$
h(t) = v_0 t + \frac{1}{2} a t^2
$$

where $h(t)$ is the height of the object at time $t$, $v_0$ is the initial velocity of the object, and $a$ is the acceleration due to gravity.  

Consider a simple hypothetical experiment investigating free fall motion. A ball is released from rest $( v_o = 0 m)$ at an initial height of approximately 125 meters and allowed to fall under the influence of gravity $( a = -9.81 m/s )$. Using a motion sensor, the ball's height is measured at regular 0.5-second intervals. Assuming negligible air resistance, the collected data is as follows:

$$
\begin{array}{|c|c|}
\hline
t (s) & h (m) \\ \hline
0 & 125.0 \\
0.5 & 123.1 \\
1.0 & 119.8 \\
1.5 & 113.6 \\
2.0 & 104.9 \\
2.5 & 93.1 \\
3.0 & 79.6 \\
3.5 & 63.1 \\
4.0 & 45.9 \\
4.5 & 24.4 \\
5.0 & 0.8 \\ \hline
\end{array}
$$


A plot of the data and the theoretical curve is shown below:

![](free_fall_plot.png)


Your task is recreate the plot shown above exactly in the file `exercise5.py`.

- Recreate all elments including but not limited to the title, axis labels, axis extents, colors, the legend.  Don't forget the horizontal line at $y=0$ (the blue line in the plot).
- The experimental data must be loaded from the provided CSV file, `free_fall_data.csv`.  You are not allowed to modify the CSV file.
- The theoretical curve should be computed using the equation above.
- The plot must be saved to a file named `free_fall_plot.png` in the current directory.
- You may only use Numpy and Matplotlib to complete this exercise. You may not use Pandas, you may not use standard Python file I/O, and you may not use any loops.


```{warning}
50% of the points for exercise 5 will be based on the following good coding practices:

- Modularity (e.g., use of functions - for example: main, load data, generate plot, etc.) 
- Use of docstrings and comments (that follows the Google style guide)
- Proper error handling (e.g., what happens if the CSV file is missing?, what happens if the image file already exists?)
```