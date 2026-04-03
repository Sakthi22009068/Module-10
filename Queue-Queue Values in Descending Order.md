# Queue-Queue Values in Descending Order Using Python 🧮

This Python program simulates a queue using a list, removes the first two elements (FIFO order), and displays the remaining values in descending order.

## 🎯 Aim

To write a Python program to:
- Accept user inputs into a list (queue)
- Remove the first two elements (simulating dequeue)
- Display the remaining values in **descending order**

## 🧠 Algorithm

1. Create an empty list `q`.
2. Read an integer `n` to determine how many elements will be added.
3. Loop `n` times:
   - Read an input value.
   - Append it to the list `q`.
4. Remove the first element using `pop(0)`.
5. Remove the second element using `pop(0)` again.
6. Sort the list in descending order.
7. Print the updated list.

## 🧪 Program: 

q = []


n = int(input("Enter number of elements: "))


for i in range(n):

    val = int(input("Enter value: "))
    
    q.append(val)

if len(q) >= 2:

    q.pop(0)
    
    q.pop(0)
    
else:

    print("Not enough elements to dequeue twice")

q.sort(reverse=True)

print("Queue after removing first two elements and sorting:")

print(q)

### Output:
Enter number of elements: 5

Enter value: 10

Enter value: 25

Enter value: 5

Enter value: 30

Enter value: 15

Queue after removing first two elements and sorting:

[30, 15, 5]

## Result:
The program successfully:

Accepts user input into a queue (list)

Removes the first two elements using FIFO principle

Displays the remaining elements in descending order
