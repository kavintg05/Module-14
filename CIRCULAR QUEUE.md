# Exp No: 36  
## Circular Queue 
---

### AIM  
To write a Python program with a function to insert float values into a Circular Queue.

---

### ALGORITHM

1. Start  
2. Check if the Circular Queue is full  
   - If `size == max_size`, print `"Queue is full"` and exit the function  
3. If the queue is not full:  
   - Read the element to be inserted  
   - Convert it to float  
   - Insert the element at the `tail` position  
   - Update tail using: `tail = (tail + 1) % max_size` (circular increment)  
   - Increment `size` by 1  
4. End

---

### PROGRAM

```
#Reg.NO-212223060119
#Name-Kavindra T G

class CircularQueue:
    def __init__(self, max_size):
        self.queue = [None] * max_size
        self.max_size = max_size
        self.head = 0
        self.tail = 0
        self.size = 0

    def insert(self, value):
        if self.size == self.max_size:
            print("Queue is full")
            return
        try:
            value = float(value)
            self.queue[self.tail] = value
            self.tail = (self.tail + 1) % self.max_size
            self.size += 1
            print(f"Inserted: {value}")
        except ValueError:
            print("Invalid input: Please enter a float value.")

    def display(self):
        if self.size == 0:
            print("Queue is empty")
            return
        index = self.head
        print("Queue elements:")
        for _ in range(self.size):
            print(self.queue[index], end=" ")
            index = (index + 1) % self.max_size
        print()

# Main Program
cq = CircularQueue(5)

cq.insert(3.5)
cq.insert(7.2)
cq.insert(1.1)
cq.insert(4.4)
cq.insert(2.6)
cq.insert(9.9)  # This should show "Queue is full"

cq.display()


```

### OUTPUT
![image](https://github.com/user-attachments/assets/c81b48f3-968a-4075-9700-4674bfe46a4e)


### RESULT
Thus, the python program with a function to insert float values into a Circular Queue has been executed and verified successfully.
