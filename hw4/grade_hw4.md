*Erik Nijkamp*  

### Overall Grade: 56/125

### Quality of report: 9/10

* Is the homework submitted (git tag time) before deadline?

	Not tagged but the last commit was made before deadline.  
	
* Is the final report in a human readable format html? 

	No `html` file. 

* Is the report prepared as a dynamic document (Jupyter notebook) for better reproducibility?  

	Yes. `ipynb`.

* Is the report clear (whole sentences, typos, grammar)? Do readers have a clear idea what's going on and how are results produced by just reading the report? (-1 pt)

	Yes. Try to include questions followed by answers. Need more explanations in answers.
 
### Correctness and efficiency of solution: 19/85 

* Q1 (5/5)

* Q2 (4/5)

	* The log-likelihood is not concave. 

* Q3, Q4 (10/10)  
	
	Note the larger memory footprint compared to Dr. Zhou's solution.  

* Q5, Q6 (0/10)

	Check Dr. Zhou's solution sketch. 

* Q7 (0/10)
	
* Q8 (0/25)

* Q9, finding the correct MLE for digits 0-9. (0/10pt)

* Q10, finding the correct LRT p-value. (0/5pt)

* Q11, achieve classification error rate 12.4%. (0/5pt)

### Usage of Git: 8/10

* Are branches (`master` and `develop`) correctly set up? Is the hw submission put into the `master` branch?

	Yes.
	
* Are there enough commits? Are commit messages clear? 
	
	Yes. 4 commits for hw4.  
	
* Is the hw4 submission tagged? (-1 pt) 

	Not tagged.

* Are the folders (`hw1`, `hw2`, ...) created correctly? 

	Yes.

* Do not put a lot auxillary files into version control.  (-1 pt)

	Make sure to exclude all those hidden `.ipynb_checkpoints` folders from version control. These folders hold auxillary files created by Jupyter. Put a line `*/.ipynb_checkpoints` in the `.gitignore` file.
	
### Reproducibility: 10/10

* Are the materials (files and instructions) submitted to the `master` branch sufficient for reproducing all the results?  

	Yes. I was able to run the Jupyter notebook and reproduce all the results.
	

* If necessary, are there clear instructions, either in report or in a separate file, how to reproduce the results?  

	Not applicable for hw4.

### Julia code style: 10/10

* Rule (4): 4 spaces for indenting. 

* Rule (6): Never place more than 80 characters on a line. 

	Some violations, e.g., code chunk [1]. 

* Rule (7): Always include a single space after a comma. 
* Rule (8):  Never insert a space before a comma.


* Rule (9): Always insert a single space before and after an operator, except for the `^` and `:` operators, which never have spaces around them. 

* Rule (12): When naming variables or functions, use short lowercase names if possible.

* Rule (13): If a variable or function name is too long to be read in all lowercase, insert underscores at word boundaries.

* Rule (16): When naming constants, use all caps.
