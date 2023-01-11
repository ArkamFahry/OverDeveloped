---
id: l97vqi680xvk9s9xo65an7i
title: Class_and_object
desc: ''
updated: 1673421974016
created: 1673421974016
isDir: false
enableToc: false
tags:
  - OOP
  - NIBM
title_imported: Class and Object
---

### Class

- A class is a template (blueprint) which is used to create objects in programming
- A class has attributes and functions 

- For Example
	- Employee
		- Attributes 
			- age
			- name
		- Functions
			- Walk
			- Work
			- Eat

- Java Example 
```Java
Class Employee {
	private int _age;
	private String _name;

	public static void Walk() {
		//walk function
	}

	public static void Work() {
		//work function
	}

	public static void Eat() {
		//eat function
	}
}
```

### Object

- Object  is used to represent any real word thing(s) or entity(s) in  a program. Any real-world entity is called an object

- A class has attributes. When an object is created from the class the attributes get values assigned to them.

- An object can have many attributes (properties) and it can preform functions (activities)

- An object can be called as a member of a class

- For Example
	- Employee
		- Attributes
			- age - 43
			- name - Gihan
		- Functions
			- Walk
			- Work
			- Eat

- Java Example
```Java
public class Main {
	public static void main(String[] args) {
		// Employee is a class
		// the employee class creates object e
		Employee e = new Employee();

		// age is an attribute and 45 assigned as the value
		e.set_age(45);

		// name is an attribute and Gihana assigned as the value
		e.set_name("Gihana");

		// Functions are activities which the object can do
		e.Walk();
		e.Work();
		e.Eat();
	}
}

class Employee {
	// all ways keep attributes private
	// So outside class can't access the value directly 
	private int _age;
	private String _name;

	// use  setters set age value 
	public void set_age(int age) {
		_age = age;
	}

	// use  setters set name value
	public void set_name(String name) {
		_name = name;
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