*Erik Nijkamp*

### Overall Grade: 81/100

### Quality of report: 8/10

* Is the homework submitted (git tag time) before deadline? (-2 pts) 

	No. `2017-04-22 00:28:19 -0700`.

* Is the final report in a human readable format html? 

	Yes. `html`.

* Is the report prepared as a dynamic document (Jupyter notebook) for better reproducibility? 

	Yes. `ipynb`.

* Is the report clear (whole sentences, typos, grammar)? Do readers have a clear idea what's going on and how are results produced by just reading the report? 

	Excellent job!

 
### Correctness and efficiency of solution: 42/50 

* Q1

* Q2 (-4 pts) 

	(2): 
	Associative rule for multiplication of floating-point numbers does not necessarilty hold. Try `x = 0.1; y = 0.2; c = 0.3`.   
	
	(3): 
	Distributive rule for floating-point numbers does not necessarily hold as well. Try `x = 0.1; y = 0.2; a = 5.0`.  
	

	(5):
	Nice example. Could also try `x = 3.0; a = 5.0`.
	
* Q3 (-2 pts) 
 
 	(1): The reason that compiler is able to unroll the loop for integer input is because fixed point numbers (integers) obey the usual associative and distributive laws.
 
	(2): The fundamental reason that the compiler does not unroll the loop as with integer input is because floating-point number arithmetic does not necessarily follow the associative and distributive laws, as you learnt in Q2. 
	
	(3): The `@fastmath` marco tells compiler to ignore the fact that floating-point number arithmetic does not necessarily follow the associative and distributive laws. Therefore compiler is able to optimize the loop like with the integer arithmetic.

* Q4	

	Catastrophic cancellation occurs in part 1. 

* Q5
	
	Have a try on the [`corrplot`](https://github.com/JuliaPlots/StatPlots.jl#corrplot-and-cornerplot) function from the `StatPlots.jl` package. 

	
* Q6 (-2 pts)

	- In your function `h1` (loop), the looping order is not optimal for Julia. Remember that Julia stores matrix in column-major order. So `ji` looping is better.  
	
### Usage of Git: 6/10

* Are branches (`master` and `develop`) correctly set up? Is the hw submission put into the `master` branch?

	Yes.

* Are there enough commits? Are commit messages clear? (-2 pts) 

	6 commits in `develop` for hw1. All commits are on 4/21 and 4/22.
**Make sure** to start version control from the very beginning of a project. Make as many commits as possible during the process. 


* Is the hw1 submission tagged?

	Yes.

* Are the folders (`hw1`, `hw2`, ...) created correctly? 

	Yes.


* Do not put a lot auxillary files into version control.  (-2 pts)  

	Make sure to exclude all those hidden `.ipynb_checkpoints` folders from version control. These folders hold auxillary files created by Jupyter. Put a line `*/.ipynb_checkpoints` in the `.gitignore` file.
	
### Reproducibility: 7/10

* Are the materials (files and instructions) submitted to the `master` branch sufficient for reproducing all the results?  (-3 pts) 

	In general, I was able to run the Jupyter notebook and reproduce all the results. Note in Q5, the path `/home/juser/M230/hw1/longley.txt` is for your own machine. Make sure your collaborators can easily run your code. You may use something like
	
	```julia
	L = readdlm(download("http://hua-zhou.github.io/teaching/biostatm280-2017spring/hw/longley.txt"))
	```
for easier reproducibility. 

* If necessary, are there clear instructions, either in report or in a separate file, how to reproduce the results?  

	Not applicable for hw1.

### Julia code style: 18/20

* Rule (4): 4 spaces for indenting.

* Rule (6): Never place more than 80 characters on a line.

* Rule (7): Always include a single space after a comma. (-2 pts)

	Some violations:   
	- Code chunk 98, lines 5, 6
	- Code chunk 33. 
	- Code chunk 58, lines 2, 3
	- ...

* Rule (8):  Never insert a space before a comma.

* Rule (9): Always insert a single space before and after an operator, except for the `^` and `:` operators, which never have spaces around them. 

* Rule (12): When naming variables or functions, use short lowercase names if possible.

* Rule (13): If a variable or function name is too long to be read in all lowercase, insert underscores at word boundaries.

* Rule (16): When naming constants, use all caps.
