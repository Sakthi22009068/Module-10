# 🔄 Types of Queue-Circular Queue in Python

This project demonstrates the implementation of a **Circular Queue** in Python. The queue accepts 3 user values, performs enqueue and dequeue operations, and displays the removed values.

---

## 🎯 Aim

To develop a Python program that implements a Circular Queue:
- Accepts 3 values from the user
- Removes the 3 values from the queue
- Displays the removed values

---

## 🧠 Algorithm

1. **Initialize** a circular queue of fixed size (e.g., 5).
2. **Define the following functions**:
   - `enqueue()`: Inserts an element into the queue.
   - `dequeue()`: Removes an element from the queue.
   - `display()`: Shows the queue contents.
3. Accept 3 values from the user using the `enqueue()` method.
4. Remove 3 values using the `dequeue()` method.
5. Print the removed values.

---

## 💻 Program:


class CircularQueue:
    def __init__(self, size):
        self.size = size
        self.queue = [None] * size
        self.front = -1
        self.rear = -1

    # Enqueue operation
    def enqueue(self, data):
        if (self.rear + 1) % self.size == self.front:
            print("Queue is Full")
        elif self.front == -1:
            self.front = 0
            self.rear = 0
            self.queue[self.rear] = data
        else:
            self.rear = (self.rear + 1) % self.size
            self.queue[self.rear] = data

    # Dequeue operation
    def dequeue(self):
        if self.front == -1:
            print("Queue is Empty")
            return None
        elif self.front == self.rear:
            temp = self.queue[self.front]
            self.front = -1
            self.rear = -1
            return temp
        else:
            temp = self.queue[self.front]
            self.front = (self.front + 1) % self.size
            return temp

    # Display queue
    def display(self):
        if self.front == -1:
            print("Queue is Empty")
        else:
            i = self.front
            while True:
                print(self.queue[i], end=" ")
                if i == self.rear:
                    break
                i = (i + 1) % self.size
            print()

cq = CircularQueue(5)


for i in range(3):
    val = int(input(f"Enter element {i+1}: "))
    cq.enqueue(val)

print("\nQueue elements:")
cq.display()


print("\nRemoved elements:")
for i in range(3):
    removed = cq.dequeue()
    if removed is not None:
        print(removed)
Add Code Here

### Output:
Enter element 1: 10
Enter element 2: 20
Enter element 3: 30

Queue elements:
10 20 30 

Removed elements:
10
20
30

## Result:
The program successfully:

Implements a Circular Queue
Accepts 3 user inputs using enqueue()
Removes elements using dequeue()
Displays the removed values correctly
