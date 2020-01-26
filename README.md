# Basics_Training

# -*- coding: utf-8 -*-
"""
Created on Wed Jan 15 21:38:54 2020
"""
# -*- coding: utf-8 -*-
"""
Created on Sun Dec 29 22:19:03 2019

@author: Sunil Magar
"""
# To confirm the version of the python

#import platform
#print('This is python version{}'.format(platform.python_version()))


import platform
def main():
    message()

def message():
    print('This is python version{}'.format(platform.python_version()))
    
if __name__ == '__main__': main()

####                                                 ####
#### Statement and Expression                        ####
####                                                 ####

# Expression is any statement that returns the result of the agreement.
# Statement line of code which may be expression

####                                                 ####
#### Whitespace and comments                         ####
####                                                 ####

import platform
def main():
    message()

def message():
    print('This is python version{}'.format(platform.python_version()))
    
    
if __name__ == '__main__': main()

print('line 2')

####                                                 ####
#### USING PRINT()                                   ####
####                                                 ####

x = 42
print('Hello, World. {}'.format(x))

print(f'Hello, world. {x}')

####                                                 ####
####           BLOCKS and SCOPE                      ####
####                                                 ####

#blocks do not decide the scope of the object but functions etc. do define.

x = 42
y = 73

if x <y:
    print('x<y: x is {} and y is {}'.format(x,y))
    
print ('something else')

####                                                 ####
####            CONDITIONS                           ####
####                                                 ####

x = 42
y = 73

if x > y:
    print('x<y: x is {} and y is {}'.format(x,y))
elif x < y:
    print('x < y: x is {} and y is {}'.format(x,y))
else:
    print('do something else')
    

####                                                 ####
####            LOOPS                                ####
####                                                 ####

#while loop
#for loop

words  = ['one', 'two', 'three', 'four', 'five' ]

n = 0
while (n < 5):
    print(words[n])
    n += 1

####                                                 ####
####        FUNCTIONS                                ####
####                                                 ####


def function(n):
    print(n)
    
function(47)

# In python all functions returns value. If return value stored in variable, it will return none. 

def function(n = 1):
    print(n)
    return n * 2
    
x = function(42)

print(x)

### Ex. 2

def isprime(n):
    if n <= 1:
        return False
    for x in range (2,n):
        if n % x == 0:
            return False
        else:
            return True
        
def list_primes():
    for n in range(100):
        if isprime(n):
            print(n, end= ' ', flush = True)
    print()

list_primes()
            

#if isprime(n):
#    print(f'{n} is prime')
#else:
#    print(f'{n} not prime')

####                                                 ####
####                         OBJECTS                 ####
####                                                 ####

# Class is definition and object is an instance of class.
# Sometimes functions are called as methods
# Variables are called as properties / class variables
# Self is the reference to the object

class Duck:
    sound = 'Quaack!'
    walking = 'Walks like a duck.'
    
    def quack(self): # Self is the reference to the object
        print(self.sound)
        
    def walk(self):
        print(self.walking)
        
def main():
    donald = Duck()  #Variable donald assining a function from class - Hence, donald become object of class Duck. 
    donald.quack()      # using the period (.) as de-reference operator to reference the member of object Donald.
    donald.walk()
    
if __name__ == '__main__': main()


####                                                 ####
####   Types and Values                              ####
####                                                 ####

x = 7
print('x is {}'.format(x))
print(type(x))

# String Type
# methods - capitalize, upper, lower, .format class

x = 'seven'.upper()
print('x is {}'.format(x))
print(type(x))

# Numberic Type
# Types  - Int, Float

from decimal import *
a = Decimal('0.10')
b = Decimal('.30')

x = a + a + a - b
#x = .1 + .1 + .1 - .3
print('x is {}'.format(x))
print(type(x))


# BOOLEAN TYPE
# Values  - True, False 
# None -- It's NoneType (inbuilt type) -- It's return false when used in boolean

# Sequency Types
# Lists, Tuples and Dictionaries

x = [1, 2, 3, 4, 5]
for i in x:
    print('i is {}'.format(i))


####                                                 ####
####                   CONDITIONALS                  ####
####                                                 ####

#IF ELIF ELSE

if False:
    print('if True')
elif False:
    print('elif True 1')
elif False:
    print('elif True 2')
elif True:
    print('elif True 3')
else:
    print('Neither True')
    
# Conditional Operators
# Comparion Operator  > == <= etc.
# Logical operator: and, or, not.
# Identity Operator: IS, IS NOT
# Membership Operator: IN, NOT IN.

# Conditional assignment

hungry = None
x = 'Feed the bear now!' if hungry else 'Do not feed the bear.'
print(x)


####                                                 ####
#### ARITHMETIC OPERATOR                             ####
####                                                 ####

# Addition, Substraction, etc.

# Bitwise Operators: &, |, ^, <<, >>

# Comparison operator

# Boolean Operators

# Operator precedence

####                                                 ####
####            LOOPS                                ####
####                                                 ####
# While loop
'If codition is true.. body of experession executed'

secret = 'Swordfish'
pw = ''

while pw != secret:
    pw = input("what's the secret word? ")

# For loop
'Use iterator or sequence to control the loop and executed for each sequency'

animals = ['bear', 'bunny', 'dog', 'cat', 'veliciraptor']

for pet in animals:
    print(pet)
    
# Additional Controls
# Continue: Used to shortcut a loop
    
# Break: Break the loop and get out of look
    
# Else: Else - if loop exit normally
    
secret = 'swordfish'

pw = ''

auth = False
count = 0
max_attemp = 5

while pw != secret:
    count += 1
    if count > max_attemp: break
    if count == 3: continue
    pw = input(f" {count}: what's the secret password?")
else:
    auth = True

print("Authorized" if auth else "calling the FBI..")


# new example
animals = ('bear', 'bunny', 'dog', 'cat', 'velociraptor')

for pet in animals:
    if pet == 'dog': continue
    #if pet == 'velociraptor': break
    print(pet)
else:
    print('that is all of the animals')
    

####                                                 ####
####        FUNCTIONS                                ####
####                                                 ####

def main():
    kitten()
    
def kitten():
    print('Meow.')
    
if __name__ == '__main__': main()

##if __name__ == '__main__': --- Equality and __main__ -- not module but content of the main file

# Python there is no distinction between function and procedures


#Function Arguments
# Non-default argument should come before the default arguments that we want to pass

def main():
    kitten(5, 6)
    
def kitten(a, b, c=0):
    print('Meow.')
    print(a, b, c)
    
if __name__ == '__main__': main()

####call by value (immutable integer etc.) vs. call by reference (mutable lists)


def main():
    x = 5
    kitten(x)
    print(f'in main: x is {x}')
    
def kitten(a):
    a = 3
    print('Meow.')
    print(a)
    
if __name__ == '__main__': main()

### Argument Lists (*args)

def main():
    kitten('meow', 'grr', 'purr')
    
def kitten(*args):
    if len(args):
        for s in args:
            print(s)
    else:
        print('Meow')
        
if __name__ == '__main__': main()

# we can call tuple or list using * in front of name like in below eg.

def main():
    x = ['meow', 'grr', 'purr']
    kitten(*x)
    
def kitten(*args):
    if len(args):
        for s in args:
            print(s)
    else:
        print('Meow')
        
if __name__ == '__main__': main()


###  KEY WORD ARGUMENTS (**kwargs)
## Note: for dictionaries use duble asteric ** if you are referencing

def main():
    kitten(Buffy = 'meow', Zilla = 'grr', Angel = 'rawr')

def kitten(**kwargs):
    if len(kwargs):
        for k in kwargs:
            print('Kitten {} says {} '.format(k, kwargs[k]))
    else:
        print('Meow.')
        
if __name__ == '__main__': main()

#### RETURN VALUES

def main():
    x = kitten()
    print(type(x), x)
    
def kitten():
    print('Meow.')
    return dict(x = 42, y = 43)
    
if __name__ == '__main__': main()


#### GENERATORS

def main():
    for i in inclusive_range(25):
        print(i, end = ' ')
    print()

def inclusive_range(*args):
    numargs = len(args)
    start = 0
    step = 1
    
    # intialize parameters
    if numargs < 1:
        raise TypeError(f'expected at least 1 argument, got{numarg}')
    elif numargs == 1:
        stop = args[0]
    elif numargs == 2:
        (start, stop) = args
    elif numargs == 3:
        (start, stop, step) = args
    else:
        raise TypeError(f'expected at most 3 arguments, got {numargs}')
        
    #generator
    i = start
    while i <= stop:
        yield i
        i += step
        
if __name__ == '__main__': main()

#### DECORATORS

def f1(f):
    def f2():
        print('This is before function call')
        f()
        print('This is after function call')
    return f2

@f1 # decorator which is wrapping f3 function inside f1
def f3():
    print('this is f3')
    
f3()


import time
def elapsed_time(f):
    def wrapper():
        t1 = time.time()
        f()
        t2 = time.time()
        print(f'Elapsed time: {(t2-t1) * 1000} ms')
    return wrapper

@elapsed_time
def big_sum():
    num_list = []
    for num in (range(0, 10000)):
        num_list.append(num)
    print(f'Big sum: {sum(num_list)}')
    
def main():
    big_sum()
    
if __name__ == '__main__': main()

#------------------------
#------------------------



####                                                 ####
#### Stuctured Data: 1. Basic data structures        ####
####                                                 ####

# list types []
# tuples ()
# Dict {}
# set {}

#### LIST & TUPLES

def main():
    game = ['Rock', 'Paper', 'Scissors', 'Lizard', 'Spock']
    print_list(game)
    
def print_list(o):
    for i in o: print(i, end=' ', flush=True)
    print()
    
if __name__ == '__main__': main()




####                                                 ####
####                        Classess                 ####
####                                                 ####

class Duck:
    sound = 'Quack quack.'
    movement = 'Walk like a duck.'
    
    def quack(self):
        print(self.sound)
        
    def move(self):
        print(self.movement)
        
def main():
    donald = Duck()
    donald.quack()
    donald.move()
    
if __name__ == '__main__': main()

### Constructing an Object

# Object is an instance of a class
# Object is created by calling a class if is  a function
#  Constuctor is used to initilize the object. 


class Animal:
    def __init__(self, type, name, sound):
        self._type = type
        self._name = name
        self._sound = sound
        
    def type(self):
        return self._type
    
    def name(self):
        return self._name
    
    def sound(self):
        return self._sound
    
def print_animal(o):
    if not isinstance(o, Animal):
        raise TypeError('print_animal(): requires an Animal')
    print('The {} is named "{}" and says "{}".'.format(o.type(), o.name(), o.sound()))
    
def main():
    a0 = Animal('Kitten', 'Fluffy', 'Rwar')
    a1 = Animal('duck', 'donald', 'quack')
    print_animal(a0)
    print_animal(a1)
    print_animal(Animal('velociraptor', 'veronica', 'hello'))
    
if __name__ == '__main__': main()


#### Class methods

# A function associated with a class is called as method.

class Animal:
    def __init__(self, **kwargs):
        self._type = kwargs['type'] if 'type' in kwargs else 'Kitten'
        self._name = kwargs['name'] if 'name' in kwargs else 'Fluffy'
        self._sound = kwargs['sound'] if 'sound' in kwargs else 'meow'
        
    def type(self, t = None):
        if t: self._type = t
        return self._type
    
    def name(self, n = None):
        if n: self._name = n
        return self._name
    
    def sound(self, s = None):
        if s: self._sound = s
        return self._sound
    
    def __str__(self): #specially named method - represent string representation of object
        return f'The {self.type()} is named "{self.name()}" and says "{self.sound}".'
    
def main():
    a0 = Animal(type='Kitten', name='Fluffy', sound='Rwar')
    a1 = Animal(type='duck', name='donald', sound='quack')
    a0.sound('bark')
    print_animal(a0)
    print_animal(a1)
        
if __name__ == '__main__': main()


###### Object data
# object data is drawn from the class and not the methods
# Hence, when you change any object - it will affect the main data
###IMP : underscore (_) inside the functions or methods indicate it's private variable and do not use it.


##### INHERITANCE

class Animal:
    def __init__(self, **kwargs):
        if 'type' in kwargs: self._type = kwargs['type']
        if 'name' in kwargs: self._name = kwargs['name']
        if 'sound' in kwargs: self._sound = kwargs['sound']

    def type(self, t = None):
        if t: self._type = t
        try: return self._type
        except AttributeError: return None

    def name(self, n = None):
        if n: self._name = n
        try: return self._name
        except AttributeError: return None

    def sound(self, s = None):
        if s: self._sound = s
        try: return self._sound
        except AttributeError: return None

class Duck(Animal):
    def __init__(self, **kwargs):
        self._type = 'duck'
        if 'type' in kwargs: del kwargs['type']
        super().__init__(**kwargs)

class Kitten(Animal):
    def __init__(self, **kwargs):
        self._type = 'kitten'
        if 'type' in kwargs: del kwargs['type']
        super().__init__(**kwargs)

def print_animal(o):
    if not isinstance(o, Animal):
        raise TypeError('print_animal(): requires an Animal')
    print(f'The {o.type()} is named "{o.name()}" and says "{o.sound()}".')

def main():
    a0 = Kitten(name = 'fluffy', sound = 'rwar')
    a1 = Duck(name = 'donald', sound = 'quack')
    print_animal(a0)
    print_animal(a1)

if __name__ == '__main__': main()

##### ITERATOR OBJECTS


class inclusive_range:
    def __init__(self, *args):
        numargs = len(args)
        self._start = 0
        self._step = 1
        
        if numargs < 1:
            raise TypeError(f'expected at least 1 argument, got {numargs}')
        elif numargs == 1:
            self._stop = args[0]
        elif numargs == 2:
            (self._start, self._stop) = args
        elif numargs == 3:
            (self._start, self._stop, self._step) = args
        else: raise TypeError(f'expected at most 3 arguments, got {numargs}')

        self._next = self._start
    
    def __iter__(self):
        return self

    def __next__(self):
        if self._next > self._stop:
            raise StopIteration
        else:
            _r = self._next
            self._next += self._step
            return _r

def main():
    for n in inclusive_range(25):
        print(n, end=' ')
    print()

if __name__ == '__main__': main()


####                                                 ####
####                HANDLING EXCEPTIONS              ####
####                                                 ####

import sys

def main():
    try: 
        x = 5/0
    except ValueError:
        print('I coaught a ValueError')
    #except ZeroDivisionError:
     #   print("don't divide by zero")
    except:
        print(f'unknown error: {sys.exc_info()[1]}')
    else:
        print('Good Job!')
        print(x)
        
    
if __name__ == '__main__': main()
    
####                                                 ####
#### String Objects                                  ####
####                                                 ####
# Common String methods

print('hello world'. upper())
print('hello world'. capatalize())
print('hello world'. title())
print('hello world'. swapcase())
print('hello world'. casefold())

# Formatting strings


####                                                 ####
####  OPENING FILES                                  ####
####                                                 ####
def main():
    f = open('lines.txt')
    for line in f:
        print(line.rstrip())
        
if __name__ == '__main__': main()





####                                                                ####
#### Data Preparation Basics : Filtering and selecting              ####
####                                                                ####

# Indexing in pandas:
# An index is a list of integers or labels you use to uniquely
#identify rows and columns

import numpy as np
import pandas as pd
from pandas import Series, DataFrame

series_obj = Series(np.arange(8), index=['row 1', 'row 2', 'row 3', 'row 4', 'row 5', 'row 6', 'row 7', 'row 8' ])
#print(series_obj)
#print(series_obj['row 7'])
#print(series_obj[[0,7]])

#np.random.seed(25)
#DF_obj = DataFrame(np.random.rand(36).reshape(6,6), 
#index = ['row 1', 'row 2', 'row 3', 'row 4', 'row 5', 'row 6' ], 
#columns = ['Column 1', 'Column 2', 'Column 3', 'Column 4', 'Column 5', 'Column 6'])
#print(DF_obj)
#print(DF_obj.loc[['row 2', 'row 5'], ['Column 5', 'Column 2']])

# Data Slicing

#print(series_obj['row 3': 'row7'])

# Comparing with scalars
#print(DF_obj < .2)

# Filteraing with Scalars
#print(series_obj[series_obj > 6])

#Setting values with scalars
series_obj['row 1', 'row 5', 'row 8'] = 8
print(series_obj)


####                                                 ####
#### Treating Mising Values                          ####
####                                                 ####

# By default, missing values are represented with NaN: 'Not a Number'
# Warning: If your dataset has 0s, 99s, or 999s, be sure to either drop or 
# approximate them as you would with missing values.

import numpy as np
import pandas as pd

from pandas import Series, DataFrame

missing = np.nan
series_obj = Series(['row 1', 'row 2', missing, 'row 4', 'row 5', 'row 6', missing, 'row 8'])
print(series_obj)


#series_obj.isnull() # return the True / False values:  For null = True; For other = False

np.random.seed(25)
DF_obj = DataFrame(np.random.rand(36).reshape(6, 6))
print(DF_obj)

DF_obj.loc[3:5, 0] = missing
DF_obj.loc[1:4, 5] = missing

print(DF_obj)

# fill with fillna

filled_DF = DF_obj.fillna(0)
print(filled_DF)

# Fill with column index
filled_DF = DF_obj.fillna({0: 0.1, 5:1.25})
print(filled_DF)

# Fill forward method

fill_DF = DF_obj.fillna(method= 'ffill') ## fill forward method
print(fill_DF)

#Counting missing values
np.random.seed(25)
DF_obj = DataFrame(np.random.rand(36).reshape(6, 6))
DF_obj.loc[3:5, 0] = missing
DF_obj.loc[1:4, 5] = missing
print(DF_obj)
DF_obj.isnull().sum()

# Filtering out missing values
DF_no_NaN = DF_obj.dropna(0)
print(DF_no_NaN)

# Column dropping
DF_no_NaN = DF_obj.dropna(axis=1)
print(DF_no_NaN)



####                                                 ####
#### REMOVING DUPLICATES                             ####
####                                                 ####

import numpy as np
import pandas as pd

from pandas import Series, DataFrame

DF_obj = DataFrame({'column1': [1, 1, 2, 2, 3, 3, 3], 
                    'column2': ['a', 'a', 'b', 'b', 'c', 'c', 'c'],
                    'column3': ['A', 'A', 'B', 'B', 'C', 'C', 'C']})
print(DF_obj)

DF_obj.duplicated() # return False and True to find that duplicate row

DF_obj.drop_duplicates()

# Droping Column Values
DF_obj = DataFrame({'column1': [1, 1, 2, 2, 3, 3, 3], 
                    'column2': ['a', 'a', 'b', 'b', 'c', 'c', 'c'],
                    'column3': ['A', 'A', 'B', 'B', 'C', 'D', 'C']})
print(DF_obj)

DF_obj.drop_duplicates(['column3'])


####                                                 ####
#### Concatenation and Transformation                ####
####                                                 ####

import numpy as np
import pandas as pd

from pandas import Series, DataFrame

DF_obj = pd.DataFrame(np.arange(36).reshape(6,6))

DF_obj_2 = pd.DataFrame(np.arange(15).reshape(5, 3))

#Concatenating Data
#Axis = 1  --- joining columns

print(pd.concat([DF_obj, DF_obj_2], axis=1))

print(pd.concat([DF_obj, DF_obj_2]))

# Transforming Data
# 1. Dropping Data

print(DF_obj.drop([0,2]))

print(DF_obj.drop([0,2], axis=1))

# 2. Adding data (by joning)

series_obj = Series(np.arange(6))
series_obj.name = "added_Variable"
print(series_obj)

variable_added = DataFrame.join(DF_obj, series_obj)

print(variable_added)

# 2. Adding data (by appending)
added_datatable = variable_added.append(variable_added, ignore_index = False)
print(added_datatable)

#in above example the index not started from next number but retained previous index. 
# use below code to re-generate the index

added_datatable = variable_added.append(variable_added, ignore_index = True)
print(added_datatable)


# 3. Sorting Data

DF_sorted = DF_obj.sort_values(by=(5), ascending=[False])
print(DF_sorted)

####                                                 ####
####        GROUPING AND AGGREGATION                 ####
####                                                 ####

# GROUPING DATA

import numpy as np
import pandas as pd

from pandas import Series, DataFrame

address = 'C:/Documents/New folder/Appraisal Documents/Python/Course 4 Python Essential Training for Data Science Part 1/Excercise files/Data/mtcars.csv'

cars = pd.read_csv(address)

cars.columns = ['car_name', 'mpg', 'cyl', 'disp', 'hp', 'drat', 'wt', 'qsec', 'vs', 'am', 'gear', 'carb']

print(cars.head())

cars_groups = cars.groupby(cars['cyl'])
print(cars_groups.mean())



####                                                           ####
#### PRACTICAL DATA VISUALIZATION: Creating Std. Data Graphics ####
####                                                           ####

# Types - 
# 1. Data Storytelling
# 2. Data Showcasing
# 3. Data art


# Chossing Graphics for Data Storytelling
# Area charts, Bar charts, Line charts
# Pie charts, Cloropleths and Point maps
# + Data showcasing = histograms, Scatter plots, Scatter plot matrices,  and raster maps

#Two methods for plot building
# 1. Functional method
# 2. Objct-oriented method

import numpy as np
from numpy.random import randn
import pandas as pd
from pandas import Series, DataFrame

import matplotlib.pyplot as plt
from matplotlib import rcParams

#Creating line chars 1. Eg
x = range(1, 10)
y = [1, 2, 3, 4, 0, 4, 3, 2, 1]

plt.plot(x, y)

#Creating line chars 2. Eg

address = 'C:/Documents/New folder/Appraisal Documents/Python/Course 4 Python Essential Training for Data Science Part 1/Excercise files/Data/mtcars.csv'

cars = pd.read_csv(address)

cars.columns = ['car_name', 'mpg', 'cyl', 'disp', 'hp', 'drat', 'wt', 'qsec', 'vs', 'am', 'gear', 'carb']

mpg = cars['mpg']

mpg.plot()

#Creating line chars 3. Eg

df = cars[['cyl', 'wt', 'mpg']]
df.plot()

#Creating Bar charts 1 eg.

plt.bar(x, y)

# creating bar charts from pandas objects

mpg.plot(kind ="bar")
mpg.plot(kind ="barh")


# Creating a pie chart

x = [1, 2, 3, 4, 0.5]
plt.pie(x)
plt.show()

# saving a plot
plt.pie(x)
plt.savefig('Pie_chart.png')
plt.show()


#########################################
######### DEFINING ELEMENTS OF A PLOT ####
########################################

# A subplot is a plotting figure that contains more than one plot or subplots

import numpy as np
from numpy.random import randn
import pandas as pd
from pandas import Series, DataFrame

import matplotlib.pyplot as plt
from matplotlib import rcParams

#%matplotlib inline
rcParams['figure.figsize']=5,4


x = range(1,10)
y = [1, 2, 3, 4, 0, 4, 3, 2, 1]

fig = plt.figure()
ax = fig.add_axes([.1, .1, 1, 1])

ax.plot(x, y)

ax.set_xlim([1,9])
ax.set_ylim([0,5])

ax.set_xticks([0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
ax.set_yticks([0, 1, 2, 3, 4, 5])

ax.plot(x,y)

###

x = range(1,10)
y = [1, 2, 3, 4, 0, 4, 3, 2, 1]

fig = plt.figure()
ax = fig.add_axes([.1, .1, 1, 1])

ax.plot(x, y)

ax.set_xlim([1,9])
ax.set_ylim([0,5])

ax.grid()
ax.plot(x,y)

### Generating multiple plots in one figure with subplots

fig = plt.figure()
fig, (ax1, ax2) = plt.subplots(1, 2)
ax1.plot(x)
ax2.plot(x,y)

#################
#################    PLOT FOMRATTING   ###############
#################

# Defining plot color

x = range(1, 10)
y = [1, 2, 3, 4, 0.5, 4, 3, 2, 1]

#plt.bar(x, y)

wide = [.5, .5, .5, .9, .9, .9, .5, .5, .5]
color = ['salmon']
plt.bar(x,y, width=wide, color=color, align='center')


####### Pandas

address = 'C:/Documents/New folder/Appraisal Documents/Python/Course 4 Python Essential Training for Data Science Part 1/Excercise files/Data/mtcars.csv'
cars = pd.read_csv(address)
cars.columns = ['car_name', 'mpg', 'cyl', 'disp', 'hp', 'drat', 'wt', 'qsec', 'vs', 'am', 'gear', 'carb']

df = cars[['cyl', 'mpg', 'wt']]
df.plot()

color_theme =  ['darkgray', 'lightsalmon', 'powderblue']
df.plot(color=color_theme)

z = [1, 2, 3, 4, .5]
plt.pie(z)
plt.show()

# using RGB color

color_theme = ['#A9A9A9', '#FFA07A', '#B0E0E6', '#FFE4C4', '#BDB76B']
plt.pie(z, colors=color_theme)
plt.show()

# Customizing line styles

x1 = range(0,10)
y1 = [10,9,8,7, 6, 5, 4,3,2,1]
plt.plot(x,y, ds='steps', lw=5)
plt.plot(x1, y1, ls='--', lw=10)

#### Setting plot markers

x1 = range(0,10)
y1 = [10,9,8,7, 6, 5, 4,3,2,1]
plt.plot(x,y, marker='1', mew=20)
plt.plot(x1, y1, marker='+', mew=15)





















































