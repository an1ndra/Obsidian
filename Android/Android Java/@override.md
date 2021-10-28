#### Why we use @Override annotation

Using @Override annotation while overriding a method is considered as a best practice for coding in java because of the following two advantages:

1) If programmer makes any mistake such as wrong method name, wrong parameter types while overriding, you would get a compile time error. As by using this annotation you instruct compiler that you are overriding this method. If you don’t use the annotation then the sub class method would behave as a new method (not the overriding method) in sub class.

2) It improves the readability of the code. So if you change the signature of overridden method then all the sub classes that overrides the particular method would throw a compilation error, which would eventually help you to change the signature in the sub classes. If you have lots of classes in your application then this annotation would really help you to identify the classes that require changes when you change the signature of a method.
```java
class ParentClass{
public void displayMethod(String msg){
System.out.println(msg);
	}
}
class SubClass extends ParentClass{
@Override
public void displayMethod(String msg){
System.out.println("Message is: "+ msg);
	}
public static void main(String args[]){
SubClass obj = new SubClass();
obj.displayMethod("Hey!!");
	}
}
```