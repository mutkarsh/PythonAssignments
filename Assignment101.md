
> 1. Print below mentioned structured. Accept input from user as no. of rows to print:
                1
               1 2
              1 2 1
            1 2 3 2 1
          1 2 3 4 3 2 1
### Solution

```python
n = int(input("enter no of rows to print."))
for i in range(1, n+1):
    for j in range(0, n-i):
        print(' '),        # print blank spaces
    for k in range(1, i+1):
        print(k),          # print no in asc order  
    for m in range(i-1, 0, -1):
        print(m),          # print no in desc order
        
    print('\r')
    
```
### Second Way

```python
n = int(input("enter no of rows to print."))
for i in range(1, n+1):
    print('  '*(n-i)),                                         # print blank spaces
    print(' '.join([str(k) for k in range(1, i+1)])),       # print no in asc order  
    print(' '.join([str(m) for m in range(i-1, 0, -1)]))   # print no in desc order
```
### Another Way

```python
n = int(input("enter no of rows to print."))
for i in range(1, n+1):
    print('  '*(n-i)),        # print blank spaces
    for k in range(1, i+1):
        print(k),          # print no in asc order  
    for m in range(i-1, 0, -1):
        print(m),          # print no in desc order
        
    print('\r')
```

> 2. Define a main function which calls another function. The second function should accept integer value as parameter and return the Fibonacci series. For example: 0, 1, 1, 2, 3, 5, 8, 13 and so on...

```python
def printFibonacci(n):
    f0, f1 = 0, 1
    for _ in range(n):
        yield f0
        f0, f1 = f1, f0+f1

if __name__=="__main__":
    print(list(printFibonacci(int(input("Enter the range of fibonacci series:")))))
```
    
