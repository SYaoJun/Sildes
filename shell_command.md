
## Linux C/C++程序员的屠龙术
- 手速快
- 设备强
- 脑子好
- 工具多

---

## 谁是脚本之王?
1. Shell 
2. Python
3. Scala
4. ...

---

## Shell中的倚天剑: SED

1. 按行操作
2. 不影响源文件
3. 支持正则表达式
4. 无所不能

---

## 热身题
- [LeetCode 195. 第十行](https://leetcode.cn/problems/tenth-line/)
```s
Line 1
Line 2
Line 3
Line 4
...
Line 9
Line 10
```

---

## 参考实现
```s [1 | 2 | 3-4]
tail -n+10 file.txt | head -1
sed -n '10p' file.txt
-n: 仅显示script处理后的结果
p: 打印匹配行
```
---

## 妙用sed的替换

```s [2 | 4 | 6]
# 用linux替换全部unix
sed 's/unix/linux/g' test.txt
# 只替换第三个
sed '3 s/unix/linux/g' test.txt
# 替换一个范围
sed '1,3 s/unix/linux/' geekfile.txt
```
- [一个神奇的Linux命令网站](https://wangchujiang.com/linux-command/c/sed.html)

---

## Shell中的屠龙刀: AWK

1. 按列处理
2. 支持正则表达式
3. 无所不能

---

## AWK获取指定行

```python
awk '{ print $2,$3 }' filename
```
#### 查看进程PID

```python
sheepxi 1234 a1
sheepfei 5678 a2
sheepman 1000 c1
```

---

## 实践出真知
#### 第十行还能这样做

```s
awk "NR==10" file.txt
```

- [LeetCode 192. 统计词频](https://leetcode.cn/problems/word-frequency/)

```s [1 | 2]
cat words.txt | xargs -n 1 | sort | 
uniq -c | sort -nr | awk '{print $2" "$1}'
```

---

## 感谢欣赏，感谢一键三连！
## 无他，唯手熟尔！

