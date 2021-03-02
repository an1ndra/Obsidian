# Graph Theory

- Path

    It is a trail in which neither vertices nor edges are repeated i.e. if we traverse a graph such that we do not repeat a vertex and nor we repeat an edge. As path is also a trail, thus it is also an open walk. Vertex not repeated. Edge not repeated.

    ![https://media.geeksforgeeks.org/wp-content/uploads/Untitled-drawing-2-2.png](https://media.geeksforgeeks.org/wp-content/uploads/Untitled-drawing-2-2.png)

    Here 6->8->3->1->2->4 is a Path

- Closed Walk

    A walk is said to be a closed walk if the starting and ending vertices are identical i.e. if a walk starts and ends at the same vertex, then it is said to be a closed walk.

    In the below diagram:

    1->2->3->4->5->3->1-> is a closed walk.

    ![Graph%20Theory%20fbf72f952055462eac7d142c3e859d54/Untitled.png](Graph%20Theory%20fbf72f952055462eac7d142c3e859d54/Untitled.png)

- Circuit

    Traversing a graph such that not an edge is repeated but vertex can be repeated and it is closed also i.e. it is a closed trail. Vertex can be repeated. Edge not repeated.

    ![Graph%20Theory%20fbf72f952055462eac7d142c3e859d54/Untitled%201.png](Graph%20Theory%20fbf72f952055462eac7d142c3e859d54/Untitled%201.png)

    Here 1->2->4->3->6->8->3->1 is a circuit

    Circuit is a closed trail. 
    These can have repeated vertices only.

- Cycle

    Traversing a graph such that we do not repeat a vertex nor we repeat a edge but the starting and ending vertex must be same i.e. we can repeat starting and ending vertex only then we get a cycle.. Vertex not repeated. Edge not repeated.

    ![Graph%20Theory%20fbf72f952055462eac7d142c3e859d54/Untitled%202.png](Graph%20Theory%20fbf72f952055462eac7d142c3e859d54/Untitled%202.png)

    Here 1->2->4->3->1 is a cycle.

- Euler Line

    A closed walk in a graph G containing all the edges of G is called an Euler line in G. 

- Euler Graph

    A graph containing an Euler line is called an Euler graph

    ![Graph%20Theory%20fbf72f952055462eac7d142c3e859d54/Screenshot_2021-02-19_032216.png](Graph%20Theory%20fbf72f952055462eac7d142c3e859d54/Screenshot_2021-02-19_032216.png)

- Euler Circuit

    The Euler Circuit is a special type of Euler path. When the starting vertex of the Euler path is also connected with the ending vertex of that path, then it is called the Euler Circuit.

    ![Graph%20Theory%20fbf72f952055462eac7d142c3e859d54/Untitled%203.png](Graph%20Theory%20fbf72f952055462eac7d142c3e859d54/Untitled%203.png)

- Euler Path

    The Euler path is a path, by which we can visit every edge exactly once. We can use the same vertices for multiple times.

    ![Graph%20Theory%20fbf72f952055462eac7d142c3e859d54/Untitled%204.png](Graph%20Theory%20fbf72f952055462eac7d142c3e859d54/Untitled%204.png)

- Hamiltonian Circuit

    A circuit is a connected graph G(V,E) is called Hamiltonian Circuit if it incudes all vertices of G.

- Hamiltonian Grap

    A connected graph G is called Hamiltonian graph if there is a cycle which includes every vertex of G and the cycle is called Hamiltonian cycle. Hamiltonian walk in graph G is a walk that passes through each vertex exactly once.

    ![Graph%20Theory%20fbf72f952055462eac7d142c3e859d54/Untitled%205.png](Graph%20Theory%20fbf72f952055462eac7d142c3e859d54/Untitled%205.png)

- Non Hamiltonian Graph

    ![Graph%20Theory%20fbf72f952055462eac7d142c3e859d54/Untitled%206.png](Graph%20Theory%20fbf72f952055462eac7d142c3e859d54/Untitled%206.png)

- Hamiltonian Path

    A Hamiltonian path, also called a **Hamilton path,** is a graph path between two vertices of a graph that visits each vertex exactly once.