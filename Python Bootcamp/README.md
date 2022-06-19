### Q&A of important/ unanswered queries from session
### Note : Please reach out :
- Email - anmolmore{at}gmail{dot}{com}
- LinkedIn - https://www.linkedin.com/in/anmol-more , please mention GL Batch.

## Week 1 :

### Can u pls explain about linspace function?
As explained in manual - https://numpy.org/doc/stable/reference/generated/numpy.linspace.html 
  
>> np.linspace(2.0, 3.0, num=5)<br/>
array([2.  , 2.25, 2.5 , 2.75, 3.  ])

>> np.linspace(2.0, 3.0, num=5, endpoint=False)<br/>
array([2. ,  2.2,  2.4,  2.6,  2.8])

>> np.linspace(2.0, 3.0, num=5, retstep=True)<br/>
(array([2.  ,  2.25,  2.5 ,  2.75,  3.  ]), 0.25)

### Does python has a compiler or interpreter ?
Python code is run using python compiler, which does step 1 - Compilation and then Interpretation<br/>
Ref : <br/>
https://towardsdatascience.com/understanding-python-bytecode-e7edaae8734d

### what is range of random numbers
Random module in python by default generates values between 0 to 1. But there are multiple functions available in random package, which gives you all possible options.<br/>
Ref - https://docs.python.org/3/library/random.html
  
### whether merge and join same
Yes, more or less they combine two arrays. My personal preference is merge because is works more like a sql query.<br/>
Ref :  https://pandas.pydata.org/docs/user_guide/merging.html

### Do we have a way to see the list of available functions of a list? like help
### whether numpy pandas are universally accepted unique libraries or there are similar packages elsewhere
### can we say all python based libraries are also open source type or commercial category
Python has thousands of packages, both open source and commercial (paid). numpy, pandas, scikit as commonly used for ML. Python is used for many many things beyond ML also. There is no single place to get all documentations. Some major documentation links are : <br/>
- https://docs.python.org/3/
- https://numpy.org
- https://pandas.pydata.org/docs/
- https://scikit-learn.org/stable/
  
We can use inbuilt help() function directly in jupyter notebook to get documentation for specific function/library

### pop and remove are same?
Overall yes, ref - https://stackoverflow.com/questions/11520492/difference-between-del-remove-and-pop-on-lists
  
### while doing square, by using the syntax, 2^2...why is giving the value 0, despite no function like this in python
^ is a XOR operation in python <br/>
** (double star) is used as power operation
  
### How can we deploy a Python Code to end user? Can we give it as a Executable file or end user will also have to install IDEs to run a Python Code?
Python file can be directly given to end user to run.<br/>
Usually client deployments in big applications are done using multiple ways, some of which I've used -
- Running python files in deployed containers, like docker, AWS lambda, GCP functions
- Deployed in python servers like Django
- Simple python servers like Flask
Ref : Detailed list of possibilies - https://stackoverflow.com/questions/52187362/how-to-deploy-python-script
  
### may I know the some particular library related to nanoscience use?
Most of python libraries specific to domain is realeased through https://pypi.org/. Try searching

### As you discussed on .pyc file, how it be generated for when file is created with .ipynb extension?
Even when we run ipynb files, pyc (python byte code) is generated. It's generated at same path, where our notebook exists.<br/>
A simple explaination on bytecode in python -  https://indianpythonista.wordpress.com/2018/01/05/demystifying-pyc-files/
  
### how tuple consume less memory comapred to list?
Tuple cannot be changed, has limited set of functionalities - so consumes less memory.<br/>
Detailed answer - https://stackoverflow.com/questions/46664007/why-do-tuples-take-less-space-in-memory-than-lists
 
### Please explain the bytes over str
In simple words - string is human readable, bytes are machine readable. This requires a deeper understanding of memory allocations. Some good reads - <br>
Ref : <br/>
- https://towardsdatascience.com/byte-string-unicode-string-raw-string-a-guide-to-all-strings-in-python-684c4c4960ba <br>
- https://towardsdatascience.com/byte-string-unicode-string-raw-string-a-guide-to-all-strings-in-python-684c4c4960ba
  
  
## Week 2

Python for Data Science Basics Cheat Sheet - https://datacamp-community-prod.s3.amazonaws.com/0eff0330-e87d-4c34-88d5-73e80cb955f2

### Difference between assignment, shallow copy, deep copy
- Assignment referes to same location as original object
- A shallow copy constructs a new object and then, inserts references into it to the objects found in the original.
- A deep copy constructs a new object all togethor
Ref : https://towardsdatascience.com/assignment-shallow-or-deep-a-story-about-pythons-memory-management-b8fad87bfa6c

### How are strings stored internally
- Python doesn't have anything called characters, strings are stored as UNICODE sequences. This article explains in detail about strings - https://medium.com/@bdov_/https-medium-com-bdov-python-objects-part-iii-string-interning-625d3c7319de <br/>
Ref : https://peps.python.org/pep-0393/

### Jupyter notebook (Interactive python terminal) print formatting is different ?
The interactive interpreter will print whatever is returned by the expression you type and execute, as a way to make testing and debugging convenient. <br/>
Ref : https://stackoverflow.com/questions/30602395/why-does-returning-in-interactive-python-print-to-sys-stdout


### Difference between zip and enumerate
- enumerate is special case of zip
- Enumerate can only process lists, where as zip can iterate through other data strcutures also.
- enumerate requires index to be monitored. Zip can help iterate multiple items at one go

They both can be used together also<br/>
  - create a list of names
  >>names = ['sravan', 'bobby', 'ojaswi', 'rohith', 'gnanesh']

  - create a list of subjects
  >>subjects = ['java', 'python', 'R', 'cpp', 'bigdata']

  - create a list of marks
  >>marks = [78, 100, 97, 89, 80]

  - use enumerate() and zip() function to iterate the lists
  >>for i, (names, subjects, marks) in enumerate(zip(names, subjects, marks)):
  >>  print(i, names, subjects, marks)

### Difference between dictionary and hashmap
https://stackoverflow.com/questions/10066374/difference-between-map-and-dict

### How to write switch case in python
This is acheived using a dictionary map and writing switcher statements corresponding to it.
https://pythonguides.com/case-statement-in-python/

### What is signature of a function
we have a signature function in inspect module. A simple example  below

>>> from inspect import signature <br/>
>>> def foo() -> None: <br/>
...   pass <br/>
...
>>> signature(foo) <br/>
<Signature () -> None>  <br/>

Ref : https://peps.python.org/pep-0362/


## Week 3 - Numpy and Pandas

### Slicing numpy arrays
https://towardsdatascience.com/slicing-numpy-arrays-like-a-ninja-e4910670ceb0

### Difference between various serialization techniques in python
https://docs.python.org/3/library/pickle.html

### Important numpy functions
https://numpy.org/doc/stable/reference/generated/numpy.empty.html


## Week 4 - Visualization

### Difference between conda and conda-forge
Doesn't makes a difference for general developement purposes<br>
https://stackoverflow.com/questions/39857289/should-conda-or-conda-forge-be-used-for-python-environments

### Important links 
- Scaling effect - https://scikit-learn.org/stable/auto_examples/preprocessing/plot_all_scaling.html
- Error bars in sns barplot - https://stackoverflow.com/questions/58362473/what-does-black-lines-on-a-seaborn-barplot-mean

