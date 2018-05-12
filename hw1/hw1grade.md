*Zhang, Zhenyu*

### Overall Grade: 90/100

### Quality of report: 10/10

* Is the homework submitted (git tag time) before deadline?

	Yes. `2018-04-23 09:55:56 -0700`.

* Is the final report in a human readable format html?  

	Yes. `html`.

* Is the report prepared as a dynamic document (Jupyter notebook) for better reproducibility?

	Yes. `ipynb`.

* Is the report clear (whole sentences, typos, grammar)? Do readers have a clear idea what's going on and how are results produced by just reading the report?

	Yes.
 
### Correctness and efficiency of solution: 46/50 

* Q1

* Q2 (-0 pts) 

Good job!
	
* Q3 (-2 pts)
 
    (3): The reason that compiler is able to unroll the loop for integer input is because fixed point numbers (integers) **obey the usual associative and distributive laws**. The fundamental reason that the compiler does not unroll the loop as with integer input is because floating-point number arithmetic does **not** necessarily follow the associative and distributive laws, as you learnt in Q2.  (-2 pts)
 
    (4): The `@fastmath` marco tells compiler to ignore the fact that floating-point number arithmetic does not necessarily follow the associative and distributive laws. Therefore compiler is able to optimize the loop like with the integer arithmetic.

 
* Q4 (-0 pts) 

	(1), (2): Apparently the expression `y = x^7 - 7x^6 + 21x^5 - 35x^4 + 35x^3 - 21x^2 + 7x -1` is mathematically equivalent to `y = (x - 1)^7`. However the first expression involves sum of terms of alternating signs and incurs **catastrophic cancellation** (substract two nearly equal numbers) (-2 pts)

* Q5 (-2 pts)
	 
     - In your function `h_loop` (loop), the looping order is not optimal for Julia. Remember that Julia stores matrix in column-major order. So `ji` looping is better.  (-2 pts)

* Q6 (-0 pts) 

Good job!
	


### Usage of Git: 8/10

* Are branches (`master` and `develop`) correctly set up? Is the hw submission put into the `master` branch?

	Yes.

* Are there enough commits? Are commit messages clear? (-2 pts)

	Only 1 commit for hw1. **Make sure** to start version control from the very beginning of a project. Make as many commits as possible during the process.  


* Is the hw1 submission tagged?

	Yes.

* Are the folders (`hw1`, `hw2`, ...) created correctly?

	Yes.	

* Do not put a lot auxillary files into version control.  

	Yes.
		

### Reproducibility: 10/10

* Are the materials (files and instructions) submitted to the `master` branch sufficient for reproducing all the results? 

    Yes

* If necessary, are there clear instructions, either in report or in a separate file, how to reproduce the results?  

    Not applicable for hw1.
    

### Julia code style: 16/20

* Rule (4): 4 spaces for indenting. (-1 pts)

    - code chunk 140, line 2

* Rule (6): Never place more than 80 characters on a line.

* Rule (7): Always include a single space after a comma.

* Rule (8):  Never insert a space before a comma.

* Rule (9): Always insert a single space before and after an operator, except for the `^` and `:` operators, which never have spaces around them. (-3 pts)

    - code chunk 10, line 11
    - code chunk 9, line 2
    - code chunk 10 in Q4, line 3
    - code chunk 42, line 1 ...

* Rule (12): When naming variables or functions, use short lowercase names if possible.

* Rule (13): If a variable or function name is too long to be read in all lowercase, insert underscores at word boundaries.

* Rule (16): When naming constants, use all caps.
