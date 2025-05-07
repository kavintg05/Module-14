# Exp.No:37  
## PRIORITY QUEUE

---

### AIM  
To write a Python program for simple implementation of Priority Queue using Queue.

---

### ALGORITHM

1. Start the program.  
2. Define a class `PriorityQueue` with an initializer to create an empty list `queue`.  
3. Define the `__str__` method to return queue elements as a string separated by spaces.  
4. Define the `isEmpty()` method to check if the queue is empty.  
5. Define the `insert(data)` method to append the given data to the queue.  
6. Define the `delete()` method to:  
   - Initialize `max_val` as 0.  
   - Loop through the queue and find the index of the maximum value.  
   - Delete and return the element at that index.  
7. In the main code, take integer input `n` for number of elements.  
8. Loop `n` times to take input values and insert them into the priority queue.  
9. Print the contents of the queue.  
10. While the queue is not empty, call `delete()` and print each returned element.  
11. End the program.

---

### PROGRAM

```
#Reg.NO-212223060119
#Name-Kavindra T G

class PriorityQueue:
    def __init__(self):
        self.queue = []

    def __str__(self):
        return ' '.join(str(i) for i in self.queue)

    def isEmpty(self):
        return len(self.queue) == 0

    def insert(self, data):
        self.queue.append(data)

    def delete(self):
        if self.isEmpty():
            return None
        max_index = 0
        for i in range(len(self.queue)):
            if self.queue[i] > self.queue[max_index]:
                max_index = i
        return self.queue.pop(max_index)

pq = PriorityQueue()
n = int(input("Enter number of elements: "))

for _ in range(n):
    val = int(input("Enter value: "))
    pq.insert(val)

print("Queue contents:")
print(pq)

print("Priority queue deletions:")
while not pq.isEmpty():
    print(pq.delete())

```

### OUTPUT

![image](https://github.com/user-attachments/assets/a30f0cba-baf2-4709-9a2e-2ca971aaad3e)

### RESULT
Thus, the python program for simple implementation of Priority Queue using Queue has been executed and verified successfully.
