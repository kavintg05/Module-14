# Exp.No:40  
## APPLICATIONS OF QUEUE

---

### AIM  
To write a Python program to implement CPU Process Scheduling using a queue.

---

### ALGORITHM  

1. Start the program.  
2. Define the function `CalculateWaitingTime(at, bt, N)`.  
3. Initialize a list `wt` of size `N` with all values set to 0.  
4. Set `wt[0] = 0` for the first process.  
5. Print the table header: "P.No.", "Arrival Time", "Burst Time", "Waiting Time".  
6. Print the values for the first process.  
7. For each process from index `1` to `N-1`:  
   - Calculate `wt[i] = (at[i - 1] + bt[i - 1] + wt[i - 1]) - at[i]`.  
   - Print the process number, arrival time, burst time, and waiting time.  
8. Initialize `total_waiting_time = 0`.  
9. Add up all waiting times.  
10. Calculate average waiting time as `average = total_waiting_time / N`.  
11. Print the average waiting time.  
12. Get burst times as input from the user for 5 processes.  
13. Call `CalculateWaitingTime()` with `at`, `bt`, and `N`.  
14. End the program.

---

### PROGRAM  

```
#Reg.NO-212223060119
#Name-Kavindra T G

def CalculateWaitingTime(at, bt, N):
    wt = [0] * N
    wt[0] = 0  

    print("\nP.No.\tArrival Time\tBurst Time\tWaiting Time")
    print(f"P1\t{at[0]}\t\t{bt[0]}\t\t{wt[0]}")

    for i in range(1, N):
        wt[i] = (at[i - 1] + bt[i - 1] + wt[i - 1]) - at[i]
        if wt[i] < 0:
            wt[i] = 0
        print(f"P{i+1}\t{at[i]}\t\t{bt[i]}\t\t{wt[i]}")

    total_waiting_time = sum(wt)
    average = total_waiting_time / N
    print(f"\nAverage Waiting Time: {average:.2f}")


N = 5
print("Enter arrival times for 5 processes:")
at = list(map(int, input().split()))
print("Enter burst times for 5 processes:")
bt = list(map(int, input().split()))

CalculateWaitingTime(at, bt, N)


```

### OUTPUT
![image](https://github.com/user-attachments/assets/a357a7ac-6fae-445b-94a8-f5427bdf8e09)


### RESULT
Thus, the python program to implement CPU Process Scheduling using a queue has been executed and verified successfully.
