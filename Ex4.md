# Ex.No:4
# Ex.Name: Write a CPP Program to insert character values in to Queue ADT  and display size of the queue,and first,Last element of the queue (use STL and set maximum size of the is 100)

## Aim:
To write a CPP Program to insert character values in to Queue ADT  and display size of the queue,and first,Last element of the queue 

## Algorithm:
1. Start the program.
2. Include queue and iostream libraries.
3. Create a queue of type char.
4. Insert characters into the queue using push().
5. Display the size of the queue using size().
6. Display the first element using front() and the last element using back().
7. End the program.

## Program:
```
#include <iostream>
#include<queue>
using namespace std;
int main()
{
    queue<char> q;
    int i,n;
    cin>>n;
    char x[n];
    for(i=1;i<=n;i++)
    {
    cin>>x[i];
    q.push(x[i]);
    }
    cout<<"Size of the Queue is:"<<q.size()<<endl;
    cout<<"The First Element of the Queue is:"<<q.front()<<endl;
    cout<<"The Last Element of the Queue is:"<<q.back();
}
```


## Output:
<img width="1111" height="488" alt="Screenshot 2025-09-20 195902" src="https://github.com/user-attachments/assets/4bad8182-38f6-4796-ad0f-0ca0964445d8" />

## Result:
The program successfully inserts character values in to Queue ADT  and display size of the queue,and first,Last element of the queue.
