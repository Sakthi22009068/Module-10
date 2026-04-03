# Stack Implementation Using `LifoQueue` (Max Size 7) 🔄

This Python program demonstrates a stack implemented using the `LifoQueue` class from the `queue` module. It allows up to 7 elements, checks if the stack is full, and then prints the elements in reverse (LIFO) order.

## 🎯 Aim

To create a Python program that:
- Implements a stack using `LifoQueue` with a maximum size of 7
- Adds user-inputted values to the stack
- Checks whether the stack is full
- Prints the stack elements in reverse order (LIFO)

## 📋 Algorithm

1. Import the `LifoQueue` class from the `queue` module.
2. Create a stack with a maximum size of 7.
3. Read the number of elements (`n`) to be added to the stack.
4. Loop `n` times:
   - Read a value from the user.
   - Use `put()` to push it onto the stack if it's not full.
5. Use `full()` to check if the stack is full and print the result.
6. Use `get()` repeatedly to pop and print elements in reverse order.

## Program
from queue import LifoQueue

stack = LifoQueue(maxsize=7)


n = int(input("Enter number of elements: "))

for i in range(n):

    if not stack.full():
    
        value = input(f"Enter element {i+1}: ")
        
        stack.put(value)
        
    else:
    
        print("Stack is full! Cannot add more elements.")
        
        break


if stack.full():

    print("\nStack is full.")
    
else:

    print("\nStack is not full.")


print("\nStack elements in reverse order (LIFO):")

while not stack.empty():

    print(stack.get())
    

## 🧪 Sample Input and Output
Enter number of elements: 5

Enter element 1: 10

Enter element 2: 20

Enter element 3: 30

Enter element 4: 40

Enter element 5: 50

Stack is not full.

Stack elements in reverse order (LIFO):

50
40
30
20
10

## Result:
The program successfully:

Implements a stack using LifoQueue

Accepts user inputs

Checks whether the stack is full

Displays elements in Last In First Out (LIFO) order
