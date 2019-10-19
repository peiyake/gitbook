# 标题

    # 一级标题
    ## 二级标题
    ### 三级标题

# 强调

    斜体：*斜体* 或者 _斜体_
    粗体：**粗体** 或者 __粗体__
    删除线：~~我是删除线~~

斜体：*斜体* 或者 _斜体_

粗体：**粗体** 或者 __粗体__

删除线：~~我是删除线~~

# 列表

### 有序列表

```
    1. 有序列表1
       1. 有序列表1子序
          1. 有序列表1子序的子序
          1. 有序列表1子序的子序
       1. 有序列表1子序
    1. 有序列表2
    1. 有序列表3
    1. 有序列表4
```

 1. 有序列表1
    1. 有序列表1子序
       1. 有序列表1子序的子序
       2. 有序列表1子序的子序
    2. 有序列表1子序
 2. 有序列表2
 3. 有序列表3
 4. 有序列表4

### 无序列表

无序列表前面使用 **+**  **-** **\***

```
    * 无序列表1
      * 无序列表1
        * 无序列表1
        * 无序列表1
      * 无序列表1
    * 无序列表1
    * 无序列表1
```

* 无序列表1
   * 无序列表1
     * 无序列表1
     * 无序列表1
   * 无序列表1
* 无序列表1
* 无序列表1

# 链接

```
    1. 链接的标准用法 [我是标准链接](https://www.google.com)
    2. 鼠标悬停时显示链接说明的用法 [例子](https://www.google.com "谷歌的主页")
    3. 相对引用链接 [例子](./README.md)
```

 1. 链接的标准用法 [我是标准链接](https://www.google.com)
 2. 鼠标悬停时显示链接说明的用法 [例子](https://www.google.com "谷歌的主页")
 3. 相对引用链接 [例子](./README.md)

# 图片 

```
     1. 标准用法
     ![考拉图片](https://avatars3.githubusercontent.com/u/16791778?v=4)
     1. 引用用法
     ![logo](./images/logo.png)
```
1. 标准用法
   ![考拉图片](https://avatars3.githubusercontent.com/u/16791778?v=4)
2. 引用用法
   ![logo](./images/logo.png)

# 表情

```
@octocat :+1: This PR looks great - it's ready to merge! :shipit:
```

@octocat :+1: This PR looks great - it's ready to merge! :shipit:

这些表情在github上支持，所有可用表情代码，请参考 (https://www.webfx.com/tools/emoji-cheat-sheet/)

# TO DO列表

```
- [x] Finish my changes
- [ ] Push my commits to GitHub
- [ ] Open a pull request
```
- [x] Finish my changes
- [ ] Push my commits to GitHub
- [ ] Open a pull request


# 表格

```
    | Tables        | Are           | Cool  |
    | ------------- |:-------------:| -----:|
    | col 3 is      | right-aligned | $1600 |
    | col 2 is      | centered      |   $12 |
    | zebra stripes | are neat      |    $1 |
```

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

# 代码高亮

markdown支持许多语言的代码高亮 可以在这里查看支持的语法高亮示例[highlight.js](https://highlightjs.org/static/demo/)

    ```c
    #include<stdio.h>
    int main(unsigned int argc,const char *argv[])
    {
        printf("Hello world\n");   
    }
    ```
    ```python
    @requires_authorization
    def somefunc(param1='', param2=0):
        r'''A docstring'''
    return (param2 - param1 + 1 + 0b10l) or None

    ```
    ```makefile
    BUILDDIR      = _build
    .PHONY: main clean
    main:
        @echo "Building main facility..."
    clean:
        rm -rf $(BUILDDIR)/*
    ```
    ```diff
    --- languages/ini.js    (revision 199)
    +++ languages/ini.js    (revision 200)
    @@ -1,8 +1,7 @@
    hljs.LANGUAGES.ini =
    {
    case_insensitive: true,
    -  defaultMode:
    -  {
    +  defaultMode: {
        contains: ['comment', 'title', 'setting'],
        illegal: '[^\\s]'
    },
    ```

```c
#include<stdio.h>
int main(unsigned int argc,const char *argv[])
{
    printf("Hello world\n");   
}
```
```python
@requires_authorization
def somefunc(param1='', param2=0):
    r'''A docstring'''
return (param2 - param1 + 1 + 0b10l) or None

```
```makefile
BUILDDIR      = _build
.PHONY: main clean
main:
    @echo "Building main facility..."
clean:
    rm -rf $(BUILDDIR)/*
```
```diff
--- languages/ini.js    (revision 199)
+++ languages/ini.js    (revision 200)
@@ -1,8 +1,7 @@
hljs.LANGUAGES.ini =
{
case_insensitive: true,
-  defaultMode:
-  {
+  defaultMode: {
    contains: ['comment', 'title', 'setting'],
    illegal: '[^\\s]'
},
```

# 水平线

    水平线：    三个或者更多 ---   

我下面有个水平线

---

# 其它内容
1. 如果想让一段文字在换行显示，可以在这段话的结尾 添加两个空格
2. 两行文字之间一个回车， 表示分行显示
3. 两行文字之间两个回车，表示分段显示
4. mark中可以直接内嵌html的代码
  
