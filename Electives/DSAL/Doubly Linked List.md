Idea is to implement a data structure that is dynamic at runtime and can easily be modified  

Downside is the slow traversal to find an item within the doubly linked list  

(Node is just an item within the linked list and can be anything)  
Uses a "head" and a "tail" to point to the next and previous nodes in the doubly linked list, instead of just a "head" in a singly linked list that only points to the next node in the list  

<br>

### Image from geeksforgeeks on doubly linked list  
![image](images/Pasted%20image%2020231105155358.png)  

<br>

### Code in C# for a node and doubly linked list  
```C#
	// In this case the node will contain a "Seat" object
    internal class Node
    {
        private Node _prev;
        private Seat _seat;
        private Node _next;

        public Node(Seat pSeat)
        {
            _seat = pSeat;
            _prev = null;
            _next = null;
        }

        public Seat Seat
        {
            get { return _seat; }
            set { _seat = value; }
        }

        public Node Next
        {
            get { return _next; }
            set { _next = value; }
        }

        public Node Prev
        {
            get { return _prev; }
            set { _prev = value; }
        }
    }

```