# # Stack-Stack Reversal Program 🔁

This Python program demonstrates how to reverse the values in a stack using basic stack operations like push and pop.

## 🎯 Aim

To write a Python program that reverses the values in a stack using standard stack operations.

## 📋 Algorithm

1. Create an empty stack.
2. Read an integer `n` from the user (number of elements to push).
3. Loop `n` times:
   - Read an integer from the user.
   - Push it onto the stack.
4. Create an empty list called `reverse`.
5. While the stack is not empty:
   - Pop the top element.
   - Append it to `reverse`.
6. Print the reversed list.


### Program:

stack = []

n = int(input("Enter number of elements: "))

for i in range(n):

    value = int(input(f"Enter element {i+1}: "))
    
    stack.append(value)


print("\nOriginal Stack:", stack)


reverse = []

while len(stack) > 0:

    reverse.append(stack.pop())

print("Reversed Stack:", reverse)



## 🧪 Sample Input and Output
Input:

Enter number of elements: 5

Enter element 1: 10

Enter element 2: 20

Enter element 3: 30

Enter element 4: 40

Enter element 5: 50

output:

Original Stack: [10, 20, 30, 40, 50]

Reversed Stack: [50, 40, 30, 20, 10]

## Result
The program successfully:

Uses a stack (list) to store elements

Applies push (append) and pop (pop) operations

Reverses the stack values correctly
