### Q&A of important/ unanswered queries from session
### Note : Please reach out on :
- Email - anmolmore<at>gmail<dot><com>
- LinkedIn - https://www.linkedin.com/in/anmol-more for queries.

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

  
### while doing square, by using the syntax, 2^2...why is giving the value 0, despite no function like this in python
^ is a XOR operation in python <br/>
** (double star) is used as power operation
  
### How can we deploy a Python Code to end user? Can we give it as a Executable file or end user will also have to install IDEs to run a Python Code?
  

  
### may I know the some particular library related to nanoscience use?
Most of python libraries specific to domain is realeased through https://pypi.org/. Try searching

### As you discussed on .pyc file, how it be generated for when file is created with .ipynb extension?
  
### how tuple consume less memory comapred to list?
Tuple cannot be changed, has limited set of functionalities - so consumes less memory.<br/>
Detailed answer - https://stackoverflow.com/questions/46664007/why-do-tuples-take-less-space-in-memory-than-lists
 
### Please explain the bytes over str
