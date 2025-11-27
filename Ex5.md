# Ex.No:5
# Ex.Name: Write a C++ Program to Check for balanced parenthesis by using Stack STL.

## Aim:
To write a C++ Program to Check for balanced parenthesis by using Stack STL.

## Algorithm:
1. Start program.
2. Read expression.
3. Create empty stack.
4. For each character: push if opening, pop if matching closing, else unbalanced.
5. After traversal, if stack empty → balanced, else → unbalanced.
6. Display result and end.

## Program:
```
#include<iostream>
#include<stack>
using namespace std;

int main() {
    stack<char> s;
    string expr;
    cin >> expr;
    bool flag = true;
    for (char ch : expr) {
        if (ch == '(' || ch == '[' || ch == '{') {
            s.push(ch);
        } 
        else if (ch == ')' || ch == ']' || ch == '}') {
            if (s.empty()) {
                flag = false;
                break;
            }
            char top = s.top();
            s.pop();  
            if ((ch == ')' && top != '(') || 
                (ch == ']' && top != '[') || 
                (ch == '}' && top != '{')) {
                flag = false;
                break;
            }
        }
    }
    
    if (!s.empty()) flag = false; 

    if (flag) {
        cout << "Balanced" << endl;
    } else {
        cout << "Not Balanced" << endl;
    }
    return 0;
}
```


## Output:
<img width="651" height="329" alt="Screenshot 2025-09-20 200430" src="https://github.com/user-attachments/assets/2770a33a-b068-495a-aece-73417ec18148" />

## Result:
The program successfully executed to Check for balanced parenthesis by using Stack STL.
