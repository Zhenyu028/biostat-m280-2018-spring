*ZHANG, ZHENYU*

### Overall Grade: 93/100

### Quality of report: 8/10

* Is the homework submitted (git tag time) before deadline? 

	Yes. `2018-05-11 22:39:26 -0700`. 

* Is the final report in a human readable format html?  

	Yes,  `html`.

* Is the report prepared as a dynamic document (Jupyter notebook) for better reproducibility?

	Yes, `ipynb`.

* Is the report clear (whole sentences, typos, grammar)? Do readers have a clear idea what's going on and how are results produced by just reading the report? (-2 pts)

Very clear report. But in question 2 part 2, the algorithm of the function is unclear. It is better to point out that woodbury formula helps to reduce computational burden. And the inverse of the matrix is avoided by Cholesky decomposition
 
### Correctness and efficiency of solution: 47/50 

* Q1 (24/25 pts)

    1, 3) (14/15 pts)
    
    **Efficiency(10/11pts)**
    Dr. Zhou's implementation for `r = 20` has memory estimate 7.12 MB and allocs estimate 10, yours is `912 allocations: 7.596 MiB`. Pretty good, but you have 912 allocations. some suggestions:
    -  Use pre-allocation to save gabbage collection: Dr. Zhou's implement uses half of the memory in pre-allocation. For more details, please check Dr. Zhou's implement(-1 pt)

     **Correctness(4/4 pts)**
    
     **Others**
    - Using `vecnorm` instead of `sum(abs2, X - A_mul_B!(mul_VW, V, W))` will speed up your function
    
    4, 5) (5/5pts) You should be able to observe that in part 5 the function ends within 3 iterations; Part 5 is not worse than the previous two. In general, the answer is on the right track
    2, 6) (5/5pts) Good job!


* Q2 (23/25 pts)

    1) (5/5pts) 
    2) (20/20 pts)
    **Algorithm(7/7pts)**
    **Efficiency(5/7pts)**
    Dr. Zhou's implementation has memory estimate 1.34KB, yours is 5.11 KB. Pretty good! Some suggestions:
    - Use `BLAS.syrk!()` to reduce memory allocation in `I + σ1^2 / σ0^2 * Symmetric(Z' * Z)` (-1 pts))
    - The extra memory allocation caused by transpose can be avoid by using Blas functions in `Z'y`. (-1 pts)
    **Correctness(6/6pts)**

    **Others**
    You can check the input to make the function more stable for wrong input.
    
### Usage of Git: 10/10

* Are branches (`master` and `develop`) correctly set up? Is the hw submission put into the `master` branch?

	Yes.

* Are there enough commits? Are commit messages clear? 

	Yes

* Is the hw2 submission tagged? 

	Yes

* Are the folders (`hw1`, `hw2`, ...) created correctly?

	Yes.	

* Do not put a lot auxillary files into version control.  

	Yes.
		

### Reproducibility: 10/10

* Are the materials (files and instructions) submitted to the `master` branch sufficient for reproducing all the results? 

	Yes

* If necessary, are there clear instructions, either in report or in a separate file, how to reproduce the results?  

	Not applicable for hw2.

### Julia code style: 18/20

* Rule (4): 4 spaces for indenting.

* Rule (6): Never place more than 80 characters on a line.

* Rule (7): Always include a single space after a comma. (-1 pts)
    - code chunk 6 line 2

* Rule (8):  Never insert a space before a comma.

* Rule (9): Always insert a single space before and after an operator, except for the `^` and `:` operators, which never have spaces around them. (-1 pt)

    - code chunk 5 last line

* Rule (12): When naming variables or functions, use short lowercase names if possible.

* Rule (13): If a variable or function name is too long to be read in all lowercase, insert underscores at word boundaries.

* Rule (16): When naming constants, use all caps.
