### 问题
Write a program that repeatedly prompts a user for integer numbers until the user enters 'done'. Once 'done' is entered, print out the largest and smallest of the numbers. If the user enters anything other than a valid number catch it with a try/except and put out an appropriate message and ignore the number. Enter the numbers from the book for problem 5.1 and Match the desired output as shown.

### 程序
```python
largest = None
smallest = None
while True:
    num = input("Enter a number: ")
    if num == "done" :
        break
    try:
        nm = float(num)
        if largest is None and smallest is None:
            smallest = nm
            largest = nm
        elif nm > largest:
            largest = nm
        elif nm < smallest:
            smallest = nm
    except:
        print("Invalid input")
        continue

print("Maximum is", int(largest))
print("Minimum is", int(smallest))
```
### 示例
```
Enter a number: un
Invalid input
Enter a number: 4
Enter a number: 5
Enter a number: 6
Enter a number: 7
Enter a number: done
Maximum is 7
Minimum is 4
```
