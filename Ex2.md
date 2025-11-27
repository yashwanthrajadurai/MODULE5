# Ex.No:2
# Ex.Name: Write a CPP Program to insert five float elements in to Stack ADT (use STL for Stack)

## Aim:
To write a CPP Program to insert five float elements in to Stack ADT (use STL for Stack)

## Algorithm:
1. Start the program.
2. Include stack and iostream libraries.
3. Create a stack of float type.
4. Take input of five float elements from the user.
5. Push each element into the stack.
6. Display elements by popping from the stack.
7. End the program.
   
## Program:
```
#include<iostream>
#include<stack>
using namespace std;
int main()
{
    stack<float> s;
    int n;
    cin>>n;
    float element;
    for(int i=0;i<n;i++)
    {
        cin>>element;
        s.push(element);
    }
    cout<<"Size of the stack: "<<n<<endl;
    while(!s.empty())
    {
        cout<<s.top()<<" ";
        s.pop();
    }
    
    
}
```


## Output:
<img width="938" height="404" alt="Screenshot 2025-09-20 195240" src="https://github.com/user-attachments/assets/c6f8054d-e2c9-4c52-ab03-a73a411dcb21" />

## Result:
The program successfully inserts float elements in to Stack ADT.
