# Queue-Remove Two String Values from the Rear End in Python 🧵

This Python program demonstrates how to manage a list of strings and remove the last two elements (i.e., from the rear of the list).

## 🎯 Aim

To write a Python program to:
- Accept `n` string values from the user
- Remove the last two values (rear end of the list)
- Display the updated list

## 🧠 Algorithm

1. Create an empty list `q`.
2. Read an integer `n` from the user (number of strings).
3. Loop `n` times:
   - Read a string input.
   - Append it to the list `q`.
4. Remove the last element using `pop()`.
5. Remove the next last element using `pop()` again.
6. Display the updated list.

##  Program:

q = []

n = int(input("Enter number of strings: "))


for i in range(n):

    val = input("Enter string: ")
    
    q.append(val)

if len(q) >= 2:

    q.pop()
    
    q.pop()
    
else:

    print("Not enough elements to remove")

print("Updated list after removing last two elements:")

print(q)



### Output:
Enter number of strings: 5

Enter string: apple

Enter string: banana

Enter string: mango

Enter string: orange

Enter string: grapes

Updated list after removing last two elements:

['apple', 'banana', 'mango']

## Result:
The program successfully:

Accepts multiple string inputs from the user

Removes the last two elements (rear end) of the list

Displays the updated list correctly
