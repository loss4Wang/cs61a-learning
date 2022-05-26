# Simple Notes for CS61A

## 1. Expression and Statement
- Expression has its own evaluation procedure. (provide values)
- Statement has its own execution procedure. (make changes)

## 2. [Pure function vs. None-Pure function](http://composingprograms.com/pages/12-elements-of-programming.html)
- Pure Func:  
Have some input and return the output applied by the function, no side effect.

- None-Pure Func:
**print func** return None and generate side effect.  
```
>>> print(print(1,2))
1
2
None
>>> None
>>> print(None)
None
```

## 3. [Confusing words](http://composingprograms.com/pages/13-defining-new-functions.html#calling-user-defined-functions)
Name Evaluation:  
A name evaluates to the value bound to that name in the **earliest frame** of the current environment in which that name is found.   
? : Don't understand what does the earliest mean?

## 4. Questions: why expressions are also statement?

## 5. Conditional statements
*else* clause is reached :
- **if** and **elif** expressions evaluate to *false value*.  

**Boolean values**:
- false value: `False, 0, None, (empty string), [empty list]`
- true value: `other numbers, True`    

Functions that perform comparisons and return boolean values typically begin with is, not followed by an underscore    
(e.g., isfinite, isdigit, isinstance, etc.)

**Short circuit**
If and and or do not short-circuit, they just return the last value; 
another way to remember this is that and and or always return the last thing they evaluate, whether they short circuit or not. 
Keep in mind that and and or don't always return booleans when using values other than True and False.


## 6. Testing
### Assertions
```
>>> def fib_test():
        assert fib(2) == 1, 'The 2nd Fibonacci number should be 1'
        assert fib(3) == 1, 'The 3rd Fibonacci number should be 1'
        assert fib(50) == 7778742049, 'Error at the 50th Fibonacci number'
```
Tests are typically written in the same file or neighboring file with the suffix _test.py.     
### [Doctests](http://composingprograms.com/pages/15-control.html)
- [doctest module](https://docs.python.org/3/library/doctest.html):
  - `from doctest import testmod`
  - `from doctest import run_docstring_examples`
  - `python3 -m doctest <file> (-v)`

A test that applies a single function is called a **unit test**. 

## 7. conditional expressions
```
<consequence> if <predicate> else <alternative>
1/x if x!= 0 else 0
```
## 8. Q: [Return Video](https://www.youtube.com/watch?v=QIh6CyrWhvw&list=PLx38hZJ5RLZfaBTgnl9EdoB3JqZl5c8G3&index=7)
Question about: search() and inverse() L6V4

## 9. Q: Write own test functions
You can also write your own functions (much like the **take_turn_test** function from Project 1).