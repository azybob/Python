## 问题：
7.1 Write a program that prompts for a file name, then opens that file and reads through the file, and print the contents of the file in upper case. Use the file words.txt to produce the output below.

## 程序：
```python
# Use words.txt as the file name
fname = open(input("Enter file name: "))
for fh in fname:
    a = fh.strip()
    print(a.upper())
```

## 示例：

```Enter file name: words.txt
[文字without double whitespace]
```
