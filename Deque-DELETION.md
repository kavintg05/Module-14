# Exp.No:38  
## Deque - DELETION

---

### AIM  
To write a Python program to delete elements at FRONT END of deque using a collection built-in function.

---

### ALGORITHM  

1. Import the `deque` class from the `collections` module.  
2. Create an empty deque.  
3. Define how many elements to input (e.g., 3 inputs as in the example).  
4. Loop through the range of input size:  
   - Read an integer from the user.  
   - Append the integer to the deque.  
5. Remove the front element of the deque using `popleft()`.  
6. Print the final deque after deletion.  

---

### PROGRAM  

```
#Reg.NO-212223060119
#Name-Kavindra T G
from collections import deque

dq = deque()

for _ in range(3):
    val = int(input("Enter a number: "))
    dq.append(val)

dq.popleft()

print("The deque after deleting from the front is:")
print(dq)


```

### OUTPUT
![image](https://github.com/user-attachments/assets/6f8809a5-919b-4a71-ab18-4e1ae7f5cac0)



### RESULT
Thus, the python program to delete elements at FRONT END of deque using a collection built-in function has been executed and verified successfully.
