# Day 13

## What I learned
- access to libraries/modules with import [module_name] as [alias_name] and use it in code [module_name].[variables/functions]
- from [module_name] import * -> access all variables and functions diretly without name of module and .
- from [module_name] import [function/variabl_name] -> access to specific variables and functions diretly in code without name of module and .
- we can explore a module with : 1-type()=know type of library and it's variables, 2-dir()=know variable of library , and 3-help()=know what library and it's variables and functions do
- submodules : modules contain variables which can refer to functions or values -> they can also have variables referring to other modules -> for example : numpy.random.randint(low=1, high=6, size=10)
- review operator overloading : for example + in numpy array is different from python list -> Understanding how Python's operators work when applied to ints, strings, and lists is no guarantee that you'll be able to immediately understand what they do when applied to a tensorflow Tensor, or a numpy ndarray, or a pandas DataFrame.
- When Python programmers want to define how operators behave on their types, they do so by implementing methods with special names beginning and ending with 2 underscores such as __lt__, __setattr__, or __contains__. Generally, names that follow this double-underscore format have a special meaning to Python.
- array.ndim -> get number of dimension
- array.size -> get total number of elements
- pattern of indexing is array[rows,columns]
- Boolean filtering : array > 200 - return an array of true/false based on condition and elements
- array[array > 200] - retrun an array of numbers that only meet the condition
- mix axis and statistics : for example np.sum(sales, axis=1)
- arange(from,to) is like range() in np -> numbers = np.arange(1,21)
- Reshaping np array : convert and change shape of np array for example from 1D to 2D -> matrix = numbers.reshape(4,5)
- np.argmax() : returns the index of the largest value -> np.argmax(months_sales)

## Exercises
- find array elements and practicing slicing
- calculate rows and columns statistics measure in a 2D np array
- reshape a 1D array to one 2D array 
- Analyse a sales array data

## Course
- Working with External Libraries From Kaggle python course
