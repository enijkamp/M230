*Erik Nijkamp*  

### Overall Grade: 89/100

### Quality of report: 10/10

* Is the homework submitted (git tag time) before deadline?

	Yes. `2017-05-18 6:18PM` for tag `hw3`. 
	
* Is the final report in a human readable format html? 

	Yes. `html`.

* Is the report prepared as a dynamic document (Jupyter notebook) for better reproducibility?  

	Yes. `ipynb`.

* Is the report clear (whole sentences, typos, grammar)? Do readers have a clear idea what's going on and how are results produced by just reading the report?

	Plenty of explanations. 
	 
### Correctness and efficiency of solution: 51/60 

* Q1 (5/5)

* Q2 (5/5)

* Q3 (10/10)  

* Q4 (21/30) 
	* code chunk [8]: A major problem is that you did not use the "sparse + low rank" structure here. You impelmentation takes `O(n^2)` flops per iteration. Using structure only takes `O(n)` flops per iteration. 
	* There's a lot of room for improving memory efficiency. For example, Dr. Zhou's implementation for the Jacobi has memory allocation 620.91 KB, while yours is 289.36MB. 
 
* Q5 (5/5)

* Q6 (5/5)



### Usage of Git: 10/10

* Are branches (`master` and `develop`) correctly set up? Is the hw submission put into the `master` branch?

	Yes.
	
* Are there enough commits? Are commit messages clear? 

	 Yes. 11 commits for hw3. 
	
* Is the hw3 submission tagged?

	Yes.

* Are the folders (`hw1`, `hw2`, ...) created correctly? 

	Yes.

* Do not put a lot auxillary files into version control.  

	Yes. 

### Reproducibility: 10/10

* Are the materials (files and instructions) submitted to the `master` branch sufficient for reproducing all the results?  

	In general I was able to run the Jupyter notebook and reproduce all the results. Note in Q3, the path `/home/juser/M230/hw3/A.txt` is for your own machine. Make sure your collaborators can easily run your code. Since you have `A.txt` and `U.txt` in the current directory, you can just use the following code.
	
	```julia 
	A = readdlm("A.txt", ',');
	U = readdlm("U.txt", ',');
	```
	Or, you can try the following code:
	
	```julia
	download("http://hua-zhou.github.io/teaching/" * 
        "biostatm280-2017spring/hw/ucla.zip")
   ```

* If necessary, are there clear instructions, either in report or in a separate file, how to reproduce the results?  

	Not applicable for hw3.

### Julia code style: 8/10

* Rule (4): 4 spaces for indenting. 

* Rule (6): Never place more than 80 characters on a line. 

* Rule (7): Always include a single space after a comma. (-2 pts) 

	* code chunk [23], [25], [26], [30], ...

* Rule (8):  Never insert a space before a comma.


* Rule (9): Always insert a single space before and after an operator, except for the `^` and `:` operators, which never have spaces around them.  


* Rule (12): When naming variables or functions, use short lowercase names if possible.

* Rule (13): If a variable or function name is too long to be read in all lowercase, insert underscores at word boundaries.

* Rule (16): When naming constants, use all caps.
