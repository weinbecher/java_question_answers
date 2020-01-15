# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the ___word___ 'polymorphism' mean?

something that has 'many forms'

2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.
     
In object-oriented programming, polymorphism refers to a programming language's ability to process objects differently depending on their data type or class. More specifically, it is the ability to redefine methods for derived classes.

     
     public interface IConnect {
       public String connect(String data);
     }
     
     public class Desktop implements IConnect {
         public String connect(String data) {
           return "connecting to network: " + data;
         }
     }
     

3. What can we use to implement polymorphism in Java?

interface



4. How many 'forms' can an object take when using polymorphism?

Inheritance and interface implementation are two "methods" used to implement polymorphism in Java. One "class" can't exist in two forms, but more than one class can implement an interface (and more than two for that matter). You can't have different "instances" of an object, but you can have different instances (objects) of a class. 

5. Give an example of when you could use polymorphism.

private ArrayList<IConnect> devices;

  public Network(String name){
      this.devices = new ArrayList<IConnect>();  
      this.name = name;
  }

public void connect(IConnect device)
       devices.add(device);  
   }
   

# Composition

6. What do we mean by 'composition' in reference to object-oriented programming?

Handling ownership from one object over to another object which it is now a part.
Composition refers to a has-a relationship where an object is made up of one or more other objects.


7. When would you use composition? Provide a simple example in Java.

Wizard can have any rides as long as it's an IFly object. Now wizard has a fly method.

    public class Wizard {
    String name;
    IFly ride;

    public Wizard(String name, IFly ride){
        this.name = name;
        this.ride = ride;
    }

    public String fly(){
        return this.ride.fly();
    }


8. What is/are the advantage(s) of using composition?

Composition allows a class to use behaviour from a group of other classes, and makes it possible for that behaviour to change at runtime.



9. When an object is destroyed, what happens to all the objects it is composed of?
still exist and can be used for other object
