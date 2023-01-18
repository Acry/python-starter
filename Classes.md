# Classes

```python
class MyClass:
    pass


myClass = MyClass() # instantiate object

print (myClass.__class__) # __main__.MyClass
print (myClass.__class__.__name__) # 'MyClass'

```

## Class Attributes

```python
class MyClass:
    myAttribute = 'a_name'


MyClass.myAttribute # access attribute

```

## Class Methods

using the `def` keyword

```python
class Student:
    def displayInfo(self): # self, refers to the calling object
        print('something')


myClass = MyClass()
myClass.displayInfo() # something

```

## Constructors

```python
class MyClass:
    def __init__(self): # constructor
        print('from constructor')
```

## Destructors

```python
class MyClass:
    def __del__(self): # destructor
        print('from destructor')

myClass = MyClass()
del myClass
```

## Instance Attributes

Instance attributes are defined in the constructor.

```python
class MyClass:
    def __init__(self): # constructor; self , refers to the calling object
        self.myAttribute = 'a_name'


MyClass.myAttribute # access attribute

```

## Class Properties

A Class Property can be defined using the `property` method.

```python
class MyClass:
    def __init__(self):
        self.__name=''
    def setname(self, name):
        self.__name=name
    def getname(self):
        return self.__name
    name=property(getname, setname)
```

It is recommended to use the property decorator instead.

```python
class MyClass:
    def __init__(self, name):
        self.__name=name

    @property
    def name(self):
        return self.__name

    @name.setter
    def name(self, value):
        self.__name = value

    @name.deleter
    def name(self, value):
        del self.__name
```
