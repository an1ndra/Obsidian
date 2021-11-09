Linked List is a part of the [Collection framework](https://www.geeksforgeeks.org/collections-in-java-2/) present in [java.util package](https://www.geeksforgeeks.org/java-util-package-java/). This class is an implementation of the [LinkedList data structure](https://www.geeksforgeeks.org/data-structures/linked-list/) which is a linear data structure where the elements are not stored in contiguous locations and every element is a separate object with a data part and address part. The elements are linked using pointers and addresses. Each element is known as a node. Due to the dynamicity and ease of insertions and deletions, they are preferred over the arrays. It also has few disadvantages like the nodes cannot be accessed directly instead we need to start from the head and follow through the link to reach to a node we wish to access.  
**Example:** The following implementation demonstrates how to create and use a linked list.   
 

Attention reader! Don’t stop learning now. Get hold of all the important DSA concepts with the [**DSA Self Paced Course**](https://practice.geeksforgeeks.org/courses/dsa-self-paced?utm_source=geeksforgeeks&utm_medium=article&utm_campaign=gfg_article_dsa_content_bottom) at a student-friendly price and become industry ready.  To complete your preparation from learning a language to DS Algo and many more,  please refer [**Complete Interview Preparation Course**](https://practice.geeksforgeeks.org/courses/complete-interview-preparation?utm_source=GeeksforGeeks&utm_medium=Text&utm_campaign=GFG_Article_Bottom_Text_CIP)**.**

In case you wish to attend **live classes** with experts, please refer [**DSA Live Classes for Working Professionals**](https://practice.geeksforgeeks.org/courses/geeks-classes-live?utm_source=geeksforgeeks&utm_medium=article&utm_campaign=gfg_article_dsa_content_bottom) and [**Competitive Programming Live for Students**](https://practice.geeksforgeeks.org/courses/competitive-programming-live?utm_source=geeksforgeeks&utm_medium=article&utm_campaign=gfg_article_cp_content_bottom).

-   Java
```java
import java.util.*;

public class Test {

	public static void main(String args[])
	{
		// Creating object of the
		// class linked list
		LinkedList<String> ll
			= new LinkedList<String>();

		// Adding elements to the linked list
		ll.add("A");
		ll.add("B");
		ll.addLast("C");
		ll.addFirst("D");
		ll.add(2, "E");

		System.out.println(ll);

		ll.remove("B");
		ll.remove(3);
		ll.removeFirst();
		ll.removeLast();

		System.out.println(ll);
	}
}
```
**Output:** 

[D, A, E, B, C]
[A]

### Performing Various Operations on LinkedList

Let’s see how to perform some basics operations on the LinkedList.  
**1. Adding Elements:** In order to add an element to an ArrayList, we can use the [add() method](https://www.geeksforgeeks.org/java-util-linkedlist-add-method-in-java/). This method is overloaded to perform multiple operations based on different parameters. They are:   
 

  

  

-   **add(Object):** This method is used to add an element at the end of the LinkedList.
-   **add(int index, Object):** This method is used to add an element at a specific index in the LinkedList.

-   Java

`// Java program to add elements` 

`// to a LinkedList`

`import` `java.util.*;` 

`public` `class` `GFG {` 

 `public` `static` `void` `main(String args[])` 

 `{` 

 `LinkedList<String> ll =` `new` `LinkedList<>();` 

 `ll.add(``"Geeks"``);` 

 `ll.add(``"Geeks"``);` 

 `ll.add(``1``,` `"For"``);` 

 `System.out.println(ll);` 

 `}` 

`}` 
```
**Output:** 

[Geeks, For, Geeks]

**2. Changing Elements:** After adding the elements, if we wish to change the element, it can be done using the [set() method](https://www.geeksforgeeks.org/linkedlist-set-method-in-java/). Since a LinkedList is indexed, the element which we wish to change is referenced by the index of the element. Therefore, this method takes an index and the updated element which needs to be inserted at that index.  
 

-   Java
```
`// Java program to change elements` 

`// in a LinkedList` 

`import` `java.util.*;` 

`public` `class` `GFG {` 

 `public` `static` `void` `main(String args[])` 

 `{` 

 `LinkedList<String> ll =` `new` `LinkedList<>();` 

 `ll.add(``"Geeks"``);` 

 `ll.add(``"Geeks"``);` 

 `ll.add(``1``,` `"Geeks"``);` 

 `System.out.println(``"Initial LinkedList "` `+ ll);` 

 `ll.set(``1``,` `"For"``);` 

 `System.out.println(``"Updated LinkedList "` `+ ll);` 

 `}` 

`}` 

**Output:** 

Initial LinkedList [Geeks, Geeks, Geeks]
Updated LinkedList [Geeks, For, Geeks]

**3. Removing Elements:** In order to remove an element from a LinkedList, we can use the [remove() method](https://www.geeksforgeeks.org/linkedlist-remove-method-in-java/). This method is overloaded to perform multiple operations based on different parameters. They are:   
 

-   **remove(Object):** This method is used to simply remove an object from the LinkedList. If there are multiple such objects, then the first occurrence of the object is removed.
-   **remove(int index):** Since a LinkedList is indexed, this method takes an integer value which simply removes the element present at that specific index in the LinkedList. After removing the element, all the elements are moved to the left to fill the space and the indices of the objects are updated.

-   Java

`// Java program to remove elements` 

`// in a LinkedList`

`import` `java.util.*;` 

`public` `class` `GFG {` 

 `public` `static` `void` `main(String args[])` 

 `{` 

 `LinkedList<String> ll =` `new` `LinkedList<>();` 

 `ll.add(``"Geeks"``);` 

 `ll.add(``"Geeks"``);` 

 `ll.add(``1``,` `"For"``);` 

 `System.out.println(` 

 `"Initial LinkedList "` `+ ll);` 

 `ll.remove(``1``);` 

 `System.out.println(` 

 `"After the Index Removal "` `+ ll);` 

 `ll.remove(``"Geeks"``);` 

 `System.out.println(` 

 `"After the Object Removal "` `+ ll);` 

 `}` 

`}` 
```
**Output:** 

Initial LinkedList [Geeks, For, Geeks]
After the Index Removal [Geeks, Geeks]
After the Object Removal [Geeks]

**4. Iterating the LinkedList:** There are multiple ways to iterate through the LinkedList. The most famous ways are by using the basic for loop in combination with a [get() method](https://www.geeksforgeeks.org/linkedlist-get-method-in-java/) to get the element at a specific index and the advanced for loop.  
 

  
  

-   Java
```java

```
**Output:** 

Geeks For Geeks 
Geeks For Geeks

[![List-ArrayList-in-Java-In-Depth-Study](https://media.geeksforgeeks.org/wp-content/uploads/20200624224531/List-ArrayList-in-Java-In-Depth-Study.png)](https://media.geeksforgeeks.org/wp-content/uploads/20200624224531/List-ArrayList-in-Java-In-Depth-Study.png)

In the above illustration, [AbstractList](https://www.geeksforgeeks.org/abstractlist-in-java-with-examples/), [CopyOnWriteArrayList](https://www.geeksforgeeks.org/copyonwritearraylist-in-java/) and the [AbstractSequentialList](https://www.geeksforgeeks.org/abstractsequentiallist-in-java-with-examples/) are the classes which implement the list interface. A separate functionality is implemented in each of the mentioned classes. They are:  
 

1.  **AbstractList:** This class is used to implement an unmodifiable list, for which one needs to only extend this AbstractList Class and implement only the get() and the size() methods.
2.  **CopyOnWriteArrayList:** This class implements the list interface. It is an enhanced version of ArrayList in which all the modifications(add, set, remove, etc.) are implemented by making a fresh copy of the list.
3.  **AbstractSequentialList:** This class implements the Collection interface and the AbstractCollection class. This class is used to implement an unmodifiable list, for which one needs to only extend this AbstractList Class and implement only the get() and the size() methods.

### How LinkedList work Internally?

Since a LinkedList acts as a dynamic array and we do not have to specify the size while creating it, the size of the list automatically increases when we dynamically add and remove items. And also, the elements are not stored in a continuous fashion. Therefore, there is no need to increase the size. Internally, the LinkedList is implemented using the [doubly linked list data structure](https://www.geeksforgeeks.org/doubly-linked-list/). The main difference between a normal linked list and a doubly LinkedList is that a doubly linked list contains an extra pointer, typically called the previous pointer, together with the next pointer and data which are there in the singly linked list.   
 

### Constructors in the LinkedList

In order to create a LinkedList, we need to create an object of the LinkedList class. The LinkedList class consists of various constructors that allow the possible creation of the list. The following are the constructors available in this class:  
 

1.  **LinkedList():** This constructor is used to create an empty linked list. If we wish to create an empty LinkedList with the name ll, then, it can be created as:   
     

> LinkedList ll = new LinkedList();   
>  

1.  **LinkedList(Collection C):** This constructor is used to create an ordered list which contains all the elements of a specified collection, as returned by the collection’s iterator. If we wish to create a linkedlist with the name ll, then, it can be created as:   
     

> LinkedList ll = new LinkedList(C);   
>  

### Methods for Java LinkedList

Method

Description

[**add(int index, E element)**](https://www.geeksforgeeks.org/java-util-linkedlist-add-method-in-java/)

This method Inserts the specified element at the specified position in this list.

[**add(E e)**](https://www.geeksforgeeks.org/java-util-linkedlist-add-method-in-java/)

This method Appends the specified element to the end of this list.

[**addAll(int index, Collection<E> c)**](https://www.geeksforgeeks.org/java-util-linkedlist-addall-method-in-java/)

This method Inserts all of the elements in the specified collection into this list, starting at the specified position.

[**addAll(Collection<E> c)**](https://www.geeksforgeeks.org/java-util-linkedlist-addall-method-in-java/)

This method Appends all of the elements in the specified collection to the end of this list, in the order that they are returned by the specified collection’s iterator.

[**addFirst(E e)**](https://www.geeksforgeeks.org/linkedlist-addfirst-method-in-java/)

This method Inserts the specified element at the beginning of this list.

[**addLast(E e)**](https://www.geeksforgeeks.org/linkedlist-addlast-method-in-java/)

This method Appends the specified element to the end of this list.

[**clear()**](https://www.geeksforgeeks.org/linkedlist-clear-method-in-java/)

This method removes all of the elements from this list.

[**clone()**](https://www.geeksforgeeks.org/linkedlist-clone-method-in-java/)

This method returns a shallow copy of this LinkedList.

[**contains(Object o)**](https://www.geeksforgeeks.org/linkedlist-contains-method-in-java/)

This method returns true if this list contains the specified element.

[**descendingIterator()**](https://www.geeksforgeeks.org/linkedlist-descendingiterator-method-in-java-with-examples/)

This method returns an iterator over the elements in this deque in reverse sequential order.

[**element()**](https://www.geeksforgeeks.org/linkedlist-element-method-in-java-with-%20examples/)

This method retrieves, but does not remove, the head (first element) of this list.

[**get(int index)**](https://www.geeksforgeeks.org/linkedlist-get-method-in-java/)

This method returns the element at the specified position in this list.

[**getFirst()**](https://www.geeksforgeeks.org/java-util-linkedlist-get-getfirst-getlast-java/)

This method returns the first element in this list.

[**getLast()**](https://www.geeksforgeeks.org/linkedlist-getlast-method-in-java/)

This method returns the last element in this list.

[**indexOf(Object o)**](https://www.geeksforgeeks.org/linkedlist-indexof-method-in-java/)

This method returns the index of the first occurrence of the specified element in this list, or -1 if this list does not contain the element.

[**lastIndexOf(Object o)**](https://www.geeksforgeeks.org/linkedlist-lastindexof-method-in-java/)

This method returns the index of the last occurrence of the specified element in this list, or -1 if this list does not contain the element.

[**listIterator(int index)**](https://www.geeksforgeeks.org/linkedlist-listiterator-method-in-java/)

This method returns a list-iterator of the elements in this list (in proper sequence), starting at the specified position in the list.

[**offer(E e)**](https://www.geeksforgeeks.org/java-util-linkedlist-offer-offerfirst-offerlast-java/)

This method Adds the specified element as the tail (last element) of this list.

[**offerFirst(E e)**](https://www.geeksforgeeks.org/java-util-linkedlist-offer-offerfirst-offerlast-java/)

This method Inserts the specified element at the front of this list.

[**offerLast(E e)**](https://www.geeksforgeeks.org/java-util-linkedlist-offer-offerfirst-offerlast-java/)

This method Inserts the specified element at the end of this list.

[**peek()**](https://www.geeksforgeeks.org/java-util-linkedlist-peek-peekfirst-peeklast-java/)

This method retrieves, but does not remove, the head (first element) of this list.

[**peekFirst()**](https://www.geeksforgeeks.org/java-util-linkedlist-peek-peekfirst-peeklast-java/)

This method retrieves, but does not remove, the first element of this list, or returns null if this list is empty.

[**peekLast()**](https://www.geeksforgeeks.org/java-util-linkedlist-peek-peekfirst-peeklast-java/)

This method retrieves, but does not remove, the last element of this list, or returns null if this list is empty.

[**poll()**](https://www.geeksforgeeks.org/java-util-linkedlist-poll-pollfirst-polllast-%20examples-java/)

This method retrieves and removes the head (first element) of this list.

[**pollFirst()**](https://www.geeksforgeeks.org/java-util-linkedlist-poll-pollfirst-polllast-%20examples-java/)

This method retrieves and removes the first element of this list, or returns null if this list is empty.

[**pollLast()**](https://www.geeksforgeeks.org/java-util-linkedlist-poll-pollfirst-polllast-%20examples-java/)

This method retrieves and removes the last element of this list, or returns null if this list is empty.

[**pop()**](https://www.geeksforgeeks.org/linkedlist-pop-method-in-java/)

This method Pops an element from the stack represented by this list.

[**push(E e)**](https://www.geeksforgeeks.org/linkedlist-push-method-in-java/)

This method Pushes an element onto the stack represented by this list.

[**remove()**](https://www.geeksforgeeks.org/linkedlist-remove-method-in-java/)

This method retrieves and removes the head (first element) of this list.

[**remove(int index)**](https://www.geeksforgeeks.org/linkedlist-remove-method-in-java/)

This method removes the element at the specified position in this list.

[**remove(Object o)**](https://www.geeksforgeeks.org/linkedlist-remove-method-in-java/)

This method removes the first occurrence of the specified element from this list, if it is present.

[**removeFirst()**](https://www.geeksforgeeks.org/linkedlist-removefirst-method-in-java/)

This method removes and returns the first element from this list.

[**removeFirstOccurrence(Object o)**](https://www.geeksforgeeks.org/linkedlist-removefirstoccurrence-method-in-%20java/)

This method removes the first occurrence of the specified element in this list (when traversing the list from head to tail).

[**removeLast()**](https://www.geeksforgeeks.org/linkedlist-removelast-method-in-java/)

This method removes and returns the last element from this list.

[**removeLastOccurrence(Object o)**](https://www.geeksforgeeks.org/linkedlist-removelastoccurrence-method-in-java-with-example/)

This method removes the last occurrence of the specified element in this list (when traversing the list from head to tail).

[**set(int index, E element)**](https://www.geeksforgeeks.org/linkedlist-set-method-in-java/)

This method replaces the element at the specified position in this list with the specified element.

[**size()**](https://www.geeksforgeeks.org/linkedlist-size-method-in-java/)

This method returns the number of elements in this list.

[**spliterator()**](https://www.geeksforgeeks.org/linkedlist-spliterator-method-in-java/)

This method Creates a late-binding and fail-fast Spliterator over the elements in this list.

[**toArray()**](https://www.geeksforgeeks.org/linkedlist-toarray-method-in-java-with-example/)

This method returns an array containing all of the elements in this list in proper sequence (from first to last element).

[**toArray(T[] a)**](https://www.geeksforgeeks.org/linkedlist-toarray-method-in-java-with-example/)

This method returns an array containing all of the elements in this list in proper sequence (from first to last element); the runtime type of the returned array is that of the specified array.

**toString()**

This method returns a String containing all of the elements in this list in proper sequence (from first to last element), each element is separated by commas and the String is enclosed in square brackets.