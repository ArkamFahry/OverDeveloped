
- Encapsulation is the process of combining Attributes and Methods in to single unit.

- The basic unit of encapsulation is the class.

- The class holds the attributes and methods

  - attributes in a class are hidden using private label
  - methods in class can be public and these methods are used to access private attributes

- Java Encapsulation Example

```Java
public class Main {
    public static void main(String[] args) {
        // Employee is a class
        // the employee class creates object e
        Employee e = new Employee();
       
		// setter methods are used to set values to private attributes
        // age is an attribute and 45 assigned as the value
        e.set_age(45);
        // name is an attribute and Gihana assigned as the value
        e.set_name("Gihana");

		// getters are used to get values from private attributes
		e.get_age();
		e.get_name();

        // Functions are activities which the object can do
        e.Walk();
        e.Work();
        e.Eat();
    }
}


/* Employee class  encapsulates all the attributes and methods the employee has like a capsule*/
class Employee {
    // all ways keep attributes private
    // So outside class can't access the value directly
    private int _age;
    private String _name;

    // use setters set age value
    public void set_age(int age) {
        _age = age;
    }

    // use setters set name value
    public void set_name(String name) {
        _name = name;
    }

    // use getters to get age value
    public int get_age() {
         return _age;
    }

    // use getters to get age value
    public String get_name() {
        return _name;
    }

    public void Walk() {
        System.out.println(_name + " Walks");
    }

    public void Work() {
        System.out.println(_name + " Works");
    }

    public void Eat() {
        System.out.println(_name + " Eats");
    }

}
```
