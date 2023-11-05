Idea is to implement a data structure that is dynamic at runtime and can easily be modified  

Main downside is the slow traversal to find an item within the doubly linked list  

(Node is just an item within the linked list and can be anything)  
Uses a "head" and a "tail" to point to the next and previous nodes in the doubly linked list, instead of just a "head" in a singly linked list that only points to the next node in the list  

<br>

### Comparison between array and linked-list from geeksforgeeks  

![image](images/Pasted%20image%2020231105155913.png)  

<br>

### Image from geeksforgeeks on doubly linked list  
![image](images/Pasted%20image%2020231105155358.png)  

<br>

### Code in C# for a node and doubly linked list in the context of a linked list of seats  
Node class  
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

<br>

Double Linked List Class  
```C#
    internal class SeatDoubleLinkedList
    {
        // "Always ensure" that this "start" refers to the first node of the list
        public Node Start { get; set; }

        public SeatDoubleLinkedList()
        {
            this.Start = null;
        }

        public void InsertAtEnd(Seat pSeatData)
        {
            Node newNode = new Node(pSeatData);

            if (this.Start == null)
            {
                this.Start = newNode;
                return;
            }

            Node p = this.Start;

            // Traverse through list till p refers to the last node
            while (p.Next != null)
            {
                p = p.Next;
            }

            p.Next = newNode;
            newNode.Prev = p;
        } // End of InsertAtEnd

        public Seat SearchByRowAndColumn(int pRow, int pColumn)
        {
            Node p = this.Start;

            while (p.Next != null)
            {
                if ((p.Seat.Column == pColumn) && (p.Seat.Row == pRow))
                {
                    // If node referenced by p satisfies
                    // the search criteria, exit the loop
                    // p will reference the node which satisfies
                    // the search criteria before exiting the while loop
                    break;
                }

                p = p.Next; // Continue to the next node
            }

            if (p == null)
            {
                return null;
            }
            else
            {
                return p.Seat;
            }
        }
    }

```