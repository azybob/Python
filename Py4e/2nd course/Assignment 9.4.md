## 问题
9.4 Write a program to read through the mbox-short.txt and figure out who has the sent the greatest number of mail messages. The program looks for 'From ' lines and takes the second word of those lines as the person who sent the mail. The program creates a Python dictionary that maps the sender's mail address to a count of the number of times they appear in the file. After the dictionary is produced, the program reads through the dictionary using a maximum loop to find the most prolific committer.

## 程序
```python
name = input("Enter file:")
if len(name) < 1 : name = "mbox-short.txt"
handle = open(name)
sns = {}

for line in handle:                                            # 判断sns中是否包含以'From '开头的行的第二个单词
    if not line.startswith('From '): continue                  # 如果包含，则为其计数 +1
    sns[line.split()[1]] = sns.get(line.split()[1],0) + 1      # 如果不包含，则将其添加进sns这个dictationary，并为其计数 +1

bw = None
bc = None
for wo,co in sns.items():
    if bc == None or bc < co:
        bw = wo
        bc = co

print(bw,bc)
```

## 示例
```
Enter file name:
```
```
cwen@iupui.edu 5
```
