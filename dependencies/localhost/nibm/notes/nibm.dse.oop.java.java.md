---
id: jnv4xlcdfy96sf83qpaf4gp
title: Java
desc: ''
updated: 1673421974016
created: 1673421974016
isDir: false
---

---
title: Java
enableToc: false
tags:
- OOP
- NIBM
---

#### Install Java JDK

- Side note need an oracle account
- Install java version 8 for stability
- Install java in the default location
- Install all the default development tools 
- Set the environment variables for java and javac

#### Facts about java

- Java is a compiled and interpreted programing language which runs on more then 3 billion devices 
- Java is used to build app for mobile application to enterprise scale server application
- Java is a statically typed language with garbage collection
- Java is also case sensitive

#### Java compiler (Javac)

- The Java compiler (javac) is the compiler which turns java source code into class files which contains  java bytecode which is run on the Java virtual machine (JVM)

#### Java virtual machine (JVM)

- Java virtual machine is used to execute the java byte code which are in java class files
- Java virtual machine is a abstract virtual machine that runs on top of the host OS.

#### Java data types

- Primitive data  types
|Type|Size|
|---|---|
|byte|1 byte|
|short|2 bytes|
|int|4 bytes|
|long|8 bytes|
|float|4 bytes|
|double|8 bytes|
|boolean|1 bit
|char|2 bytes|

- Non primitive data types
	- String
	- Array

#### Compiling and Running java 

- Create a java file with a name and ".java" file extension
	- Ex -: main.java

- Write some java source code in it
```Java
public class main {
	public static void main(String[] args) {
		System.out.println("Hello World");
	}
}
```
- Then navigate to that files location using cmd (bash for OSX, Linux)

- Using the java compiler (javac) compile the java source file
```
D:\Projects\Java> javac main.java
```
- Javac will compile the source code and output a class file
	- Ex -: main.class

- Using the java virtual machine run the java class file which contains the java byte code
```
D:\Projects\Java> java main // do not put the class extension it will throw an error
```
- The output will be "Hello World"

-  After editing the source code always re-compile the source file before running it

#### Example java code

##### Input and output in java

- Input and output in java
```Java
public class InputAndOutput {
	public static void main(String args[]) {
		int num1, num2, result;

		System.out.print("Enter num 1 : ");
		num1 = Integer.parseInt(System.console().readLine());

		System.out.print("Enter num 2 : ");
		num2 = Integer.parseInt(System.console().readLine());

		result=num1+num2;
		System.out.println("Sum is = " + result);
	}
}
```
##### Selection in java

- If else in java 
```Java
public class IfElse {
    public static void main(String[] args) {
        int num;
        
        System.out.print("Enter num : ");
        num = Integer.parseInt(System.console().readLine());

        if(num>100) {
            System.out.print("Excellent");
        } else if(num>80) {
            System.out.print("Good");
        } else if(num>60) {
            System.out.print("Average");
        } else {
            System.out.print("Fail");
        }
    }
}
```

- Switch in java 
```Java
public class Hello {
	public static void main(String[] args) {
		int num;

		System.out.print("Enter num : ");
		num = Integer.parseInt(System.console().readLine());
		
		switch(num) {
			case 90:
				System.out.println("A");
				break;
			case 70:
				System.out.println("B");
				break;
			default:
				System.out.println("C");
				break;
		}
	}
}
```

-  Condition operator  (Ternary operator)
```Java
public class Hello {
	public static void main(String[] args) {
		int num;

		System.out.print("Enter num : ");
		num = Integer.parseInt(System.console().readLine());
		
		String msg = num > 10 ? "Greater than 10" : "Less than 10";
		System.out.print(msg);
	}
}
```
##### Casting values in java 

- Casting higher value to lower value
```Java
public class CastHigherToLower {
	public static void main(String[] args) {
		float a = 100;
		int b;
		b=(int)a;
		System.out.println(b);
	}
}

public class CastHigherToLower {
	public static void main(String[] args) {
		byte a;
		int b = 100;
		a=(byte)b;
		System.out.println(b);
	}
}
```

- Cast lower value to higher value
```Java
public class CastLowerToHiger {
	public static void main(String[] args) {
		int a = 100;
		float b;
		b=a;
		System.out.println(b);
	}
}

public class CastLowerToHiger {
	public static void main(String[] args) {
		float a = 100;
		double b;
		b=a;
		System.out.println(b);
	}
}
```
##### Java data type conversions

- String to int
```Java
public class StringToInt {
	public static void main(String args[]) {
		String value = "100";
		int x = Integer.parseInt(value);
		System.out.println(x);
	}
}
```

- String to Float
```Java
public class StringToFloat {
	public static void main(String args[]) {
		String value = "100";
		float x = Float.parseFloat(value);
		System.out.println(x);
	}
}
```

- String to Double
 ```Java
public class StringToDouble {
	public static void main(String args[]) {
		String value = "100";
		double x = Double.parseDouble(value);
		System.out.println(x);
	}
}
```

- Parse to String
```Java
public class ParseToString {
	public static void main(String args[]) {
		int value = 100;
		String x = String.valueOf(value);
		System.out.println(x);
	}
}
```