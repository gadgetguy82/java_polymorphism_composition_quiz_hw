# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the ___word___ 'polymorphism' mean?<br />
In OO programming polymorphism refers to when an object can be considered as an instance of multiple types at the same time.
This is done via the use of inheritance and interfaces in Java. Objects inheriting from the same parent class or
implementing the same interfaces can be considered as the same type.

2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.<br />
This means that an object will have more than one ___is-a___ relationship.
```Java
public abstract class Phone {
  private String make;
  private int[] numbers;
  public Phone(String make) {
    this.make = make;
    this.numbers = new int[]{ 1,2,3,4,5,6,7,8,9,0 };
  }

  public int dial(int number) {
    return number;
  }
}
```
```Java
public interface IPhoto {
  public void takePhoto();
}
```
```Java
public class MobilePhone extends Phone implements IPhoto {
  private ArrayList<Picture> pictures
  public MobilePhone(String make) {
    super(make);
  }

  public void takePhoto(Picture picture) {
    this.pictures.add(picture);
  }
}
```

3. What can we use to implement polymorphism in Java?<br />
In Java this done via inheriting from a parent class or implementing one or more interfaces.

4. How many 'forms' can an object take when using polymorphism?<br />
As many as the object needs to represent its properties and methods.

5. Give an example of when you could use polymorphism.<br />
You could use it in chain inheritance where an apple extends from a fruit class which in turn extends from a food class.
The created object from the apple class is an instance of apple, fruit and food at the same time.


# Composition

6. What do we mean by 'composition' in reference to object-oriented programming?<br />
Composition is when an object is made up of one or many other objects.

7. When would you use composition? Provide a simple example in Java.<br />
You would use composition when there is a ___has-a___ relationship.
```Java
public class Bathtub {
  private int size;
  private boolean filled;
  public Bathtub(int size) {
    this.size = size;
  }

  public void fill() {
    this.filled = true;
  }

  public void empty() {
    this.filled = false;
  }
}
```
```Java
public class Toilet {
  private boolean full, clogged;
  public Toilet() {
    this.full = false;
    this.clogged = false;
  }

  public void flush() {
    this.full = false;
  }

  public void use(Person person) {
    person.discharge();
    this.full = true;
  }
}
```
```Java
public class Bathroom {
  private int size;
  private Bathtub bathtub;
  private Toilet toilet;
  public Bathroom(int size, Bathtub bathtub, Toilet toilet) {
    this.size = size;
    this.bathtub = bathtub;
    this.toilet = toilet;
  }
}
```
The above code shows composition in that a **Bathroom** has a **Bathtub** and a **Toilet**.

8. What is/are the advantage(s) of using composition?<br />
Composition is more flexible in that you can switch out components depending on the behaviour you want.
It is easier to test the component class methods over having to test all the sub-class' super-class methods.

9. When an object is destroyed, what happens to all the objects it is composed of?<br />
The other objects are destroyed inside the object but any independant instances outside would remain.
