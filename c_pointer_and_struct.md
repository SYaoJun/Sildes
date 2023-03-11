## 大纲
- 指针
- 结构体
- 文件IO

----

## C语言中的指针
- 变量
- 地址
- 8字节

---
## 一级指针

```c
  int num = 18;
  int *ptr = &num;
```
---

## 二级指针

```c
  int num = 18;
  int *ptr = &num;
  int **ptr_ptr = &ptr;
```
---

## 结构体

```c
struct book {
     char title[MAXTITL];
     char author[MAXAUTL];
     float value;
};
```
---

## 文件IO

```c
fread(&stus[0], sizeof(Stu_T), 1, fp);
fwrite(&stus[0], sizeof(Stu_T), 1, fp);
```
---

## 参考文献
1. [知乎@姚军](https://www.zhihu.com/people/wan-yi-er-89)
2. [Stanford CS107](https://web.stanford.edu/class/cs107a/index.html#calendar)
3. [C Primer Plus](https://item.jd.com/12627795.html)