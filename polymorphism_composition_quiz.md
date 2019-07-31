# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the ___word___ 'polymorphism' mean?<br />
In OO programming polymorphism refers to when an object can be considered as multiple types at the same time.
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

4. How many 'forms' can an object take when using polymorphism?<br />

5. Give an example of when you could use polymorphism.<br />



# Composition

6. What do we mean by 'composition' in reference to object-oriented programming?<br />

7. When would you use composition? Provide a simple example in Java.<br />

8. What is/are the advantage(s) of using composition?<br />

9. When an object is destroyed, what happens to all the objects it is composed of?<br />
