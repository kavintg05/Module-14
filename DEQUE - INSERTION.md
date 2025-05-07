# Exp.No:39  
## DEQUE - INSERTION

---

### AIM  
To write a Python program to insert elements at REAR END of deque using a collection built-in function.

---

### ALGORITHM  

1. Import the `deque` class from the `collections` module.  
2. Initialize an empty deque.  
3. Start an infinite loop using `while True`.  
4. In each iteration, take input from the user.  
5. If the input is an empty string, break the loop.  
6. If the input is not empty, convert it to an integer and append it to the deque.  
7. After the loop ends, append the values `14` and `15` to the deque.  
8. Print the message `"The deque after appending at right is :"`.  
9. Print the contents of the deque.  

---

### PROGRAM  

```
#Reg.NO-212223060119
#Name-Kavindra T G

```python
from collections import deque

dq = deque()

while True:
    user_input = input("Enter a number (or press Enter to stop): ")
    if user_input == '':
        break
    try:
        dq.append(int(user_input))
    except ValueError:
        print("Invalid input. Please enter an integer.")

dq.append(14)
dq.append(15)

print("The deque after appending at right is:")
print(dq)
```




### OUTPUT
![image](https://github.com/user-attachments/assets/d9c7c109-e150-4169-8a1f-a5ce5e627145)


### RESULT
Thus, the python program to insert elements at REAR END of deque using a collection built-in function has been executed and verified successfully.
