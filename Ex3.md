# Ex.No:3
# Ex.Name: write a C++ program to implement FCFS algorithm (to read no of.process p1,p2,p3 and p4 and its burst time  from the user )& find out waiting time,turn around time,average waiting time & average turn around time?

## Aim:
To write a C++ program to implement FCFS algorithm.

## Algorithm:
1. Start the program.
2. Read number of processes (here 4) and their burst times from user.
3. Initialize waiting time of first process to 0.
4. Calculate waiting time for other processes: waiting[i] = waiting[i-1] + burst[i-1].
5. Calculate turn-around time: turnaround[i] = waiting[i] + burst[i].
6. Compute total waiting time and total turnaround time.
7. Find average waiting time and average turnaround time.
8. Display waiting time, turn-around time for each process and averages.
9. End program.

## Program:
```
#include <iostream>
#include <queue>
using namespace std;

int main(){
    cout << "Processes   BT time   WT time   TA time" << endl;
    queue<int> processes;
    int a;
    for(int i=0;i<4;i++){
        cin >> a;
        processes.push(a);
    }
    int wt=0,ta=0,i=1,cn=0,wn=0;
    while(!processes.empty()){
        wn += wt;
        ta+=processes.front();
        cn += ta;
        cout << "       " << i << "       " << processes.front() << "       " << wt << "       " << ta << endl;
        wt+=processes.front();
        processes.pop();
        i++;
    }
    cout << "Average waiting time = " << wn/4.0 << endl;
    cout << "Average turn around time = " << cn/4.0 << endl;
}
```

## Output:
<img width="1127" height="777" alt="Screenshot 2025-09-20 195612" src="https://github.com/user-attachments/assets/b043a4e7-ba4b-40df-8c86-bc918a166a6d" />

## Result:
Thus the program correctly implements FCFS Scheduling.
