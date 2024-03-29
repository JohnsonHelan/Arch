# 1级标题 Markdown手册
## 2级标题
### 3级标题

## 段落
换行方式通常有两种  
第一种是“两个空格”  

第二种是“使用空行”
## 字体
*斜体*  
_斜体_  
**粗体**  
__斜体__  
****斜粗****  
____斜粗____

## 分割线
可在一行中应用三个以上的星号、减号或底线来建立分割线
***
星号  
* * *
减号  
- - -
下划线
___

## 删除线
~~文本两端加上“波浪线”，即可添加删除线~~

## 下划线
<u> 可通过“尖括号+u”, 来实现下划线</u>

## 脚注
XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

## 列表
### 无序列表
* a
* b
* c
+ d
+ e
+ f
- g
- h
- i

### 有序列表
1. a
    * aa
        * aaa
2. b
    * bb
3. c
    * 3.3. cc
        * 3.3.1. ccc

### 区块
#### 区块中使用列表
#### 列表中使用区块
1. a
> 列表区块  
>> 区块列表  
>>> 多级区块  
>    * aa
>        * aaa


### 代码
#### 代码区块
##### 前后各三个停顿号包裹
```
int main(void)
{
    printf("hello world");
    
    return 0;
}
```

#### 四个空格标注（每行）
    
    int gets(void *ptr);
    int puts(void *ptr);

## 链接
[链接名称](https://www.runoob.com)  


### 高级链接（涉及到变量定义）
文档正文中定义链接[连接地址][URL]，其中URL为变量；
文档末尾定义变量

[URL]: https://www.runoob.com

## 图片
未完待续

## 表格
表头，单元格，对齐方式
| 表头1 | 表头2 |
| ----  | ---- |
| a     | 单元格字符至少被一对空格环绕 |
| c     | d    |

| 左对齐 | 右对齐 | 中间对齐 |
| :----- | ----: | :-: |
| a      |     b | c |
| d      |     e | f |

## 高级技巧
#### 支持HTML元素
XXXXXXXXXXXXXXXXXXXXXXXXX
#### 转义

__支持以下符号前加\\来实现以下符号的输出：
```
\   反斜线
`   反引号
*   星号
_   下划线
{}  花括号
[]  方括号
()  小括号
#   井字号
+   加号
-   减号
.   英文句点
!   感叹号
```
eq:
> \*\*粗体字符\*\*, 可实现粗体的输出
