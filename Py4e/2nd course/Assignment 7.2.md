## 问题：
7.2 Write a program that prompts for a file name, then opens that file and reads through the file, looking for lines of the form:
X-DSPAM-Confidence:    0.8475
Count these lines and extract the floating point values from each of the lines and compute the average of those values and produce an output as shown below. Do not use the sum() function or a variable named sum in your solution.

## 程序：
```python
# Use the file name mbox-short.txt as the file name
fname = input("Enter file name: ")
fh = open(fname)
a = 0
b = 0
for line in fh:
    if not line.startswith("X-DSPAM-Confidence:") : continue
    a = a + 1
    b = b + float(line[line.find('0'):])
print('Average spam confidence:',b/a)
```

## 示例：

```
Enter file name: mbox-short.txt
```
```
Average spam confidence: 0.750718518519
```
