# Queue
# QUEUE IN CPP

Aim: To study and implement Queues in CPP.

Tools Used: VS Code or Programiz online compiler.

# Theory

## Queues in Cpp
A queue is a linear data structure that follows the First-In-First-Out (FIFO) principle, where elements are inserted at the rear and removed from the front. Queues are commonly used in scheduling, buffer management, and resource sharing. In C++, they can be implemented using arrays, linked lists, or the STL queue class. The primary operations of a queue are enqueue (to insert an element) and dequeue (to remove an element), while front and rear operations allow access to the first and last elements, respectively. Queues can be either fixed-size (static) or dynamic, depending on the implementation. Variants of queues include circular queues, priority queues, and double-ended queues (deque). Queues are essential for managing data in an orderly manner, ensuring sequential processing where the order of arrival is preserved.

```

#include <iostream>
using namespace std;

class Queue {
private:
    int front, rear, size;
    int* arr;

public:
    // Constructor
    Queue(int s) {
        size = s;
        arr = new int[size];
        front = 0;
        rear = -1;
    }

    // Enqueue operation
    void enqueue(int value);

    // Dequeue operation
    void dequeue();

    // Display queue
    void display();

    // Check if queue is empty
    bool isEmpty();

    // Check if queue is full
    bool isFull();
};

```

**--> Key Points:**
1. Traversal requires moving sequentially from front to rear.
2. Dynamic queues grow or shrink at runtime, while static queues have a fixed size.

# Program-1: Array-Based Implementation of Queue in Cpp
This program demonstrates a queue implemented using a fixed-size array in C++. The queue follows the FIFO (First-In-First-Out) principle, where elements are inserted at the rear and removed from the front. The enqueue function adds elements to the queue, while checking for overflow, and the dequeue function removes elements, handling underflow. The display function shows all elements currently in the queue from front to rear. This array-based implementation provides a simple and efficient way to manage sequential data, though its size is fixed.

--> Algorithm:

1. Start
2. Define a class Queue with:
  --An integer array arr[SIZE] to store elements.
  --Two integers front and back to track the first and last elements.
3. Initialize front = -1 and back = -1 in the constructor.
4. Enqueue operation:
  --Check if back == SIZE - 1 → if yes, print "Queue Overflow".
  --If front == -1, set front = 0.
  --Increment back and store the value at arr[back].
5. Dequeue operation:
  --Check if front == -1 or front > back → if yes, print "Queue Underflow".
  --Print arr[front] as removed element.
  --Increment front to remove the element.
6. Display operation:
  --If queue is empty (front == -1 or front > back), print "Queue is empty".
  --Else, traverse from front to back and print each element.
7. Stop

# Conclusion
Queues are a linear data structure that follow the FIFO (First-In-First-Out) principle. Array-based queues allow insertion at the rear and deletion from the front efficiently, though their size is fixed. They are useful in applications like scheduling, buffering, and sequential data processing. Overall, queues help manage data in an orderly and sequential manner.
