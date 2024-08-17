# OOPS in Python Programming

- Class
- Object
- Polymorphism
- Encapsulation
- Inheritance
- Abstraction

# OOPs (Object-Oriented Programming) in Python

## 1. Class : A class is a blueprint for creating objects. It defines a set of attributes and methods that the created objects will have. Think of it as a template for the objects.

   ```python
   class Hello:
       # Constructor method
       def __init__(self, name, greet):
           self.name = name
           self.greet = greet
       
       # Method to print greeting
       def wish(self):
           print(f"Hello {self.name}, {self.greet}")
   ```

## 2. Object: An object is an instance of a class. It is created based on the class and has access to the class’s attributes and methods. Objects encapsulate data and behavior.

   ```python
   c = Hello("Anubhav", "how are you?")
   c.wish()  # Output: Hello Anubhav, how are you?
   ```

## 3. Polymorphism: Polymorphism allows objects of different classes to be treated as objects of a common superclass. It provides a way to perform a single action in different forms. For example, different classes can have methods with the same name but different implementations.

   ```python
   class Dog:
       def sound(self):
           return "Bark"
   
   class Cat:
       def sound(self):
           return "Meow"
   
   def make_sound(animal):
       print(animal.sound())
   
   d = Dog()
   c = Cat()
   make_sound(d)  # Output: Bark
   make_sound(c)  # Output: Meow
   ```

## 4. Encapsulation: Encapsulation involves bundling data and methods that operate on that data within a single unit, typically a class. It restricts direct access to some of an object's components, which can prevent accidental modification.

   ```python
   class Person:
       def __init__(self, name):
           self.__name = name  # Private attribute
       
       def get_name(self):
           return self.__name
       
       def set_name(self, name):
           self.__name = name
   
   p = Person("John")
   print(p.get_name())  # Output: John
   p.set_name("Doe")
   print(p.get_name())  # Output: Doe
   ```

## 5. Inheritance: Inheritance allows a class to inherit attributes and methods from another class. This promotes code reuse and establishes a relationship between classes.

   ```python
   class Animal:
       def sound(self):
           return "Some sound"
   
   class Dog(Animal):
       def sound(self):
           return "Bark"
   
   d = Dog()
   print(d.sound())  # Output: Bark
   ```

## 6. Abstraction: Abstraction means hiding the complex implementation details and showing only the necessary features of an object. It allows focusing on what an object does rather than how it does it.

   ```python
   from abc import ABC, abstractmethod
   
   class AbstractAnimal(ABC):
       @abstractmethod
       def sound(self):
           pass
   
   class Dog(AbstractAnimal):
       def sound(self):
           return "Bark"
   
   d = Dog()
   print(d.sound())  # Output: Bark
```

### Method Overloading

Since Python doesn't support method overloading directly, you can use default arguments to simulate it:

```python
class Greet:
    def say_hello(self, name=None):
        if name:
            return f"Hello, {name}!"
        else:
            return "Hello, World!"

# Create an instance of Greet
greet = Greet()

# Method calls
print(greet.say_hello())      # Output: Hello, World!
print(greet.say_hello("Alice"))  # Output: Hello, Alice!
```

In this example, the `say_hello` method handles both cases where a name is provided and where it is not, mimicking method overloading.

### Method Overriding

Here's a simple example of method overriding:

```python
class Animal:
    def make_sound(self):
        return "Some generic sound"

class Cat(Animal):
    def make_sound(self):
        return "Meow"

# Create instances
animal = Animal()
cat = Cat()

# Method calls
print(animal.make_sound())  # Output: Some generic sound
print(cat.make_sound())     # Output: Meow
