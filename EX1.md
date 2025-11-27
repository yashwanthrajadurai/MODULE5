# Ex.No:1
# Ex.Name: Write a CPP program for Infix To Postfix Conversion using Stack STL

## Aim:
To write a CPP program for Infix To Postfix Conversion using Stack STL

## Algorithm:
1. Start the program.
2. Define precedence function for operators.
3. Traverse infix expression character by character.
4. If operand → add to result.
5. If ( → push to stack.
6. If ) → pop from stack until (.
7. If operator → pop operators from stack with higher or equal precedence, then push current.
8. After traversal, pop remaining stack operators to result.
9. Display postfix expression.
10. End program.

## Program:
```
#include <iostream>
#include <stack>
#include <string>
#include <cctype>

using namespace std;

// Function to get the precedence of operators
int precedence(char op) {
    switch (op) {
        case '+':
        case '-':
            return 1;
        case '*':
        case '/':
            return 2;
        case '^':
            return 3;
        default:
            return 0;
    }
}

// Function to check if the character is an operator
bool isOperator(char c) {
    return (c == '+' || c == '-' || c == '*' || c == '/' || c == '^');
}

// Function to convert infix expression to postfix expression
string infixToPostfix(const string &infix) {
    stack<char> s;
    string postfix = "";

    for (char c : infix) {
        if (isspace(c)) {
            continue; // Skip spaces
        } else if (isdigit(c) || isalpha(c)) {
            postfix += c; // Add operands to postfix expression
        } else if (c == '(') {
            s.push(c); // Push '(' onto stack
        } else if (c == ')') {
            // Pop and output from the stack until '(' is encountered
            while (!s.empty() && s.top() != '(') {
                postfix += s.top();
                s.pop();
            }
            s.pop(); // Remove '(' from stack
        } else if (isOperator(c)) {
            // Pop from stack while top of stack has higher or equal precedence
            while (!s.empty() && precedence(s.top()) >= precedence(c)) {
                postfix += s.top();
                s.pop();
            }
            s.push(c); // Push current operator onto stack
        }
    }

    // Pop all the remaining operators from the stack
    while (!s.empty()) {
        postfix += s.top();
        s.pop();
    }

    return postfix;
}

int main() {
    string infix;
    getline(cin, infix);

    string postfix = infixToPostfix(infix);
    cout << "Postfix is : " << postfix << endl;

    return 0;
}
```


## Output:
<img width="1095" height="362" alt="Screenshot 2025-09-20 194831" src="https://github.com/user-attachments/assets/19c7bf91-60ed-4fea-8ff4-c96f44774aa7" />

## Result:
The program successfully executed for Infix To Postfix Conversion using Stack STL.
