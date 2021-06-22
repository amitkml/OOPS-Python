# What is Cloure?

To understand the concept of closures, we need to understand some basic concepts like nested functions and free variables. Nested functions in Python are the functions which are defined inside another function.
![im](https://miro.medium.com/max/1480/1*NamyWBedolrH4-N3iwUMfw.png)

## Nested Function
```
#nested function example
def outer_function():
    x=10
    print("It is outer function which encloses a nested function")
    def nested_function():
        print("I am in nested function and I can access x from my enclosing function's scope. Printing x")
        print(x)
    nested_function()

#Execution
outer_function() 
```
## What is a free variable?
It is a variable if we declare a variable inside a function or a block then it can be used only inside that function or block.x is a free variable in above example. Here nested_function can reference x because a function has access to the variables defined in the scope where it is defined.

## What are closures in Python?
Closures in Python are used in object oriented programming by which a nested function remembers and has access to variables in the scope of the function in which it is defined.
- We need to have nested functions.
- Nested function needs to refer to variables defined in its outer scope i.e the outer function.
- The third and most important condition for a closure to exist is that the outer function must return the nested function.

## Why should we use closures in Python?
Closures in Python can be used if we want to refrain from using global variables and thus can be used for data hiding. A very good usage of closures is done when decorators are implemented.
