### 问题：
Write a program to prompt for a score between 0.0 and 1.0. If the score is out of range, print an error. If the score is between 0.0 and 1.0, print a grade using the following table:
Score Grade
\>= 0.9 A
\>= 0.8 B
\>= 0.7 C
\>= 0.6 D
\< 0.6 F
If the user enters a value out of range, print a suitable error message and exit. For the test, enter a score of 0.85.

### 程序：
```python
score = input("Enter Score: ")
try: 
    s = float(score)    #! 尝试将字符串score转化为float并赋值于变量s
except: 
    print("Error! Please enter a numeric input!")
    quit()              #! 如果无法将string转换为float则输出错误提示并退出此次程序执行
                        #! 如果转换成功，则开始执行接下来的if-elif-else语句
if s < 0.0 or s > 1.0:
    print("Error! Please enter a numeric input between 0.0 and 1.0")
    quit()              #! 如果无用户输入数值超过给定的范围则输出错误提示并退出此次程序执行
elif s >= 0.9:
    g = 'A'
elif s >= 0.8:
    g = 'B'
elif s >= 0.7:
    g = 'C'
elif s >= 0.6:
    g = 'D'
else:
    g = 'F'
print(g)
```
### 示例：
`input : 1.2`</br>
`output: Error! Please enter a numeric input between 0.0 and 1.0`

`input : one`</br>
`output: Error! Please enter a numeric input!`

`input : 0.85`</br>
`output: B`
