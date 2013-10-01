---
layout: post
title: "Recap Of OOP Concepts"
date: 2013-09-02 18:39
comments: true
categories: 
published: true
---

Wow, OOP ([Object-Oriented Programming](http://en.wikipedia.org/wiki/Object-oriented_programming#History)) is way older than me and may be you. Well, how much of it's concepts do we know. I'll use the ruby code below to give a recap on some of the concepts in OOP.


Out Pet class definition with two methods

~~~ ruby
class Pet
  # This method call creates both getters and setters for each variable passed
  attr_accessor :name, :color

  def initialize(name, color)
    @name  = name
    @color = color
  end

  def greet
    puts "Hi, meet #{@name}, my lovely pet."
  end
end
~~~

The Cat class inherits from Pet and overrides the "greet" method

~~~ ruby
# Cat inherits from Pet which is the superclass in this case
class Cat < Pet

  def greet
    puts "Meow"
  end
end
~~~


The Dog class inherits from Pet and overrides the "greet" method as well

~~~ ruby
# Dog is another subclass that inherits from Pet as well
class Dog < Pet

  def greet
    puts "Woof"
  end
end
~~~


### Objects & Classes  
Objects model real-world objects and can be seen as "black boxes" that encapsulate attributes and behaviours. Eg, if "Pet" is the object, the attributes are name, color, etc. If "Dog" is the object, one unique behaviour is barking.

Classes are the main stuff. You can think of them as templates or blueprints that objects immitate. Hence, an object is called "an instance" of a class. From the code above, Pet, Cat and Dog are classes.

>Imagine you are filling a form, the blank form is analogous to a class whiles a filled form is analogous to an object. The blank form is a blueprint (Class), but the filled form is unique to you (Object). The code snippets below give examples of objects that are based on the classes defined above.

~~~ ruby
# Asuming we have a brown dog called Jack
# Here we create an instance (jack) of the Dog class
jack = Dog.new("Jack", "Brown")

# Lets create another one
my_pet = Cat.new("Pretty Pet", "Black and White")
~~~

Classes have methods which define the behaviours of the object in question. Let's take a look at the "greet" method on Pet.

~~~ ruby
# For "jack" which is a Dog,
jack.greet # Prints "Woof"

# For my_pet which is a Cat,
my_pet.greet # Prints "Meow"
~~~


### Coming next are Inheritance, Encapsulation etc
