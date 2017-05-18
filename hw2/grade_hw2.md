*Eric Nijkamp* 

### Overall Grade: 81/100

### Quality of report: 8/10

* Is the homework submitted (git tag time) before deadline?

	Yes. `2017-05-02 18:15:33 -0700`.
	
* Is the final report in a human readable format html? 

	Yes. `html`.

* Is the report prepared as a dynamic document (Jupyter notebook) for better reproducibility? 

	Yes. `ipynb`.

* Is the report clear (whole sentences, typos, grammar)? Do readers have a clear idea what's going on and how are results produced by just reading the report? (-2 pts)

	 Need more description of the question and explanation of your solutions and algorithmic choices, esp Q1 and Q3. One year later can you still remember what you are doing by just reading your report? Some details can be improved. E.g., boldface matrices and vectors in LaTeX.
	 
	  
### Correctness and efficiency of solution: 38/50 

* Q1 (13/20)

	 It's good you do sanity check for the correctness of `kinship` function. Dr. Zhou's implementation has memory allocation 7.64MB, while yours is 198.67MB. There is a lot of room for improving efficiency. Some comments: 
  	
	* Code chunk 1, function `e3`: Matrix multiplication is the major computation as you noticed. But the two matrix multiplications can be merged into a single one, cutting computational cost by half. 	
	* Code chunk 1, function `e3`: Because `X * X'` is symmetric, compuation can be saved using BLAS-3 function `BLAS.syrk`. 
	* Code chunk 8, line 5-6: Calcuation of `p` and `sum_p` can be achieved by a single double-loop.  
	* Do check your solution against the Dr. Zhou's solution sketch to understand why. 

* Q2 (10/10)
	
	Good job!



* Q3 (15/20) 
 
 	Dr. Zhou's implementation has memory allocation 3.09KB, while yours is 122.39MB. There is a lot of room for improvement:   
 	* Utilize the Woodbury formula and the determinant formula in Question 2. 
	* Do check your solutions against Dr. Zhou's implementation and understand why.


### Usage of Git: 10/10

* Are branches (`master` and `develop`) correctly set up? Is the hw submission put into the `master` branch?

	Yes.


* Are there enough commits? Are commit messages clear?

	Yes. 6 commits in `develop` for hw2. I expect more frequent commits, which will be precious for your long term projects and also for backup purpose. 


* Is the hw2 submission tagged?

	Yes.

* Are the folders (`hw1`, `hw2`, ...) created correctly? 

	Yes.

* Do not put a lot auxillary files into version control. (Giving you 2 points back since you did not get feedback on homework 1 after submitting homework 2.)  

	Make sure to exclude all those hidden `.ipynb_checkpoints` folders from version control. These folders hold auxillary files created by Jupyter. Put a line `*/.ipynb_checkpoints` in the `.gitignore` file.
	
### Reproducibility: 10/10

* Are the materials (files and instructions) submitted to the `master` branch sufficient for reproducing all the results?  

	Yes.

* If necessary, are there clear instructions, either in report or in a separate file, how to reproduce the results?  

	Not applicable for hw2.

### Julia code style: 15/20

* Rule (4): 4 spaces for indenting. 

* Rule (6): Never place more than 80 characters on a line. (-1 pt) 

	* Code chunk 13, line 5

* Rule (7): Always include a single space after a comma. (-2 pts)

	Some violations. For example:  
	- Code chunk 1, lines 3, 7, ...  
	- ...

* Rule (8):  Never insert a space before a comma.

* Rule (9): Always insert a single space before and after an operator, except for the `^` and `:` operators, which never have spaces around them. (-2 pts)

	Many violations. For example:
	- Code chunk 1, lines 7: insert space around `*`, `+` and `-`.
	- ...

* Rule (12): When naming variables or functions, use short lowercase names if possible.

* Rule (13): If a variable or function name is too long to be read in all lowercase, insert underscores at word boundaries.

* Rule (16): When naming constants, use all caps.
