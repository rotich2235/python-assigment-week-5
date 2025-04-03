# python-assigment-week-5
**Assignment 1: Design Your Own Class! 🏗️
Create a class representing anything you like (a Smartphone, Book, or even a Superhero!).
Add attributes and methods to bring the class to life!
Use constructors to initialize each object with unique values.
Add an inheritance layer to explore polymorphism or encapsulation.**
class Smartphone:
    """A class representing a smartphone."""
    def __init__(self, brand, model, price):
        self.brand = brand
        self.model = model
        self.__price = price  # Encapsulation: Private attribute

    def get_price(self):
        return self.__price

    def set_price(self, new_price):
        if new_price > 0:
            self.__price = new_price
        else:
            print("Price must be positive!")

    def specs(self):
        return f"{self.brand} {self.model} costs ${self.__price}"


class GamingSmartphone(Smartphone):
    """A subclass representing a gaming smartphone."""
    def __init__(self, brand, model, price, gpu):
        super().__init__(brand, model, price)
        self.gpu = gpu

    def gaming_specs(self):
        return f"{self.brand} {self.model} has a powerful {self.gpu} GPU for gaming!"
      
       
   **Activity 2: Polymorphism Challenge! 🎭**
   
 Create a program that includes animals or vehicles with the same action (like move()). However, make each class define move() differently (for example, Car.move() prints "Driving" 🚗, while Plane.move() prints "Flying" ✈️).

class Vehicle:
    """Base class representing a generic vehicle."""
    def move(self):
        pass  # To be implemented by subclasses


class Car(Vehicle):
    def move(self):
        return "Driving 🚗"


class Plane(Vehicle):
    def move(self):
        return "Flying ✈️"


class Boat(Vehicle):
    def move(self):
        return "Sailing ⛵"


 


