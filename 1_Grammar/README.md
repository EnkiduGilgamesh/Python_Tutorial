# 1 Grammar

## Function

### Basic

Packaging code in `function`s to realize a specific function can make program more readable convenient. A `function` in python is like this

```python
def func_name(args_list):
    
    statements

    return
```

For instance

```python
def cmpBigger(a, b):
    if a > b:
        return a
    else:
        return b
```

After we define a function, we can call it in our main program.

```python
res = cmpBigger(10, 20)
print(res)
```

In python, the *args_list* and *return* is not essential. For instance

```python
def hello():
    print("Hello, world!")


hello()
```

### Named Argument

When we transmit arguments to a function, the order must be the same with the *argument list* in function. However, there is another way to transmit arguments to function with a less strict order. Use the `cmpBigger` as a example

```python
res = cmpBigger(b=20, a=10)
print(res)
```

If the argument is named, the order is essential. But notice that if there are both named argument and unnamed argument in one arguments list, the named argument must follow the unnamed argument. For example

```python
def exam(a, b, c, d, e, f):
    pass


exam(1, 2, 3, f=6, e=5, d=4)
# This is an incorrect way to call the function 
# exam(f=6, e=5, d=4, 1, 2, 3)
```

### Default Argument

In some situations, not all the arguments are essential when transmitting. So we can set a default value for some argument when defining a function. For instance

```python
def exam(a, b, c, d=4):
    pass


exam(1, 2, 3)
```

If we don't transmit the value of `d` to the function, the value will defaultly set `4`. But if we transmit a value, the value will change into what we transmit.

Also, notice that the default argument must follow the normal argument. The function definition underneath is illegal.

```python
def exam(d=4, a, b, c):
    pass
```

### 
