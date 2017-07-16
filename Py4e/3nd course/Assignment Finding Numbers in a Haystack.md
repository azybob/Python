## 问题
### Finding Numbers in a Haystack
In this assignment you will read through and parse a file with text and numbers. You will extract all the numbers in the file and compute the sum of the numbers.

### Data Files
We provide two files for this assignment. One is a sample file where we give you the sum for your testing and the other is the actual data you need to process for the assignment.

Sample data: http://py4e-data.dr-chuck.net/regex_sum_42.txt (There are 90 values with a sum=445833)
Actual data: http://py4e-data.dr-chuck.net/regex_sum_6917.txt (There are 82 values and the sum ends with 489)
These links open in a new window. Make sure to save the file into the same folder as you will be writing your Python program. Note: Each student will have a distinct data file for the assignment - so only use your own data file for analysis.

There can be any number of numbers in each line (including none)
## 程序
```python
import re
fh = open('regex_sum_6917.txt').read()
sum = 0
for i in re.findall('[0-9]+', fh):
    sum = sum + int(i)
print(sum)


# import re
# print( sum( [ int(i) for i in re.findall('[0-9]+',open('regex_sum_6917.txt').read())]))

# 以上和以下的一行代码, 简单来说, 就是：
# int(i)是函数, 通过遍历所有从'regex_sum_6917.txt', 这个文件中读取的, 
# 仅包含数字的元素, 然后进行int(), 取整, 最后求和得到结果。

# import re
# print( sum( [ int(i) for i in re.findall('[0-9]+',open(input('Enter file name:\n'),'r').read())]))
```

## 示例
```378489```
