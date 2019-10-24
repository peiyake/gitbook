# 简单理解海明码

> 本文内容来自互联网，原文连接：(http://baijiahao.baidu.com/s?id=1598006039749022275&wfr=spider&for=pc)


二进制数据经过传送、存取等环节，会发生误码(1变成0或0变成1)，这就有如何发现及纠正误码的问题。所有解决此类问题的方法就是在原始数据(数码位)基础上增加几位校验位。我们常使用的检验码有三种. 分别是奇偶校验码、海明校验码和循环冗余校验码(CRC)。

海明校验码是由RichardHamming于1950年提出、目前还被广泛采用的一种很有效的校验方法。它的实现原理，是在k个数据位之外加上r个校验位，从而形成一个k+r位的新的码字，使新的码字的码距比较均匀地拉大。把数据的每一个二进制位分配在几个不同的偶校验位的组合中，当某一位出错后，就会引起相关的几个校验位的值发生变化，这不但可以发现出错，还能指出是哪一位出错，为进一步自动纠错提供了依据。但是因为这种海明校验的方法只能检测和纠正一位出错的情况。所以如果有多个错误，就不能查出了。

**什么是码距？**

两个码组对应位上数字的不同位的个数称为码组的距离，简称码距，又称海明（Hamming）距离。例如00110和00100码距为1，12345和13344码距为2，Caus和Daun码距为2。

海明校验码公式（假设为k个数据位设置r个校验位）

    2 ^ r -1 >= k + r

公式怎么得出来的呢？

    假设有r个校验位，一个位子有0或1两种情况，r个位子就有2^r种排列情况，能表示2^r种状态。其中一个状态用来表示正确（没有错误发生）的这种情况。其余的2^r-1种状态来表示错误发生在哪一位。总共有k+r位，所以2^r-1一定要>=总位子k+r。

按照该不等可以得出k与r的对应关系

    2^r -1 -r >= k

| k值(数据位数) | r值(校验码位数) |
|-----|------|
|1|2|
|2~4|2|
|5~11|3|
|12~16|4|
|...|...|

**注意：海明校验码是放在2的幂次位上的，即“1,2,4,8,16,32······”**

实战求1011的海明码

第一步：求r的值（即校验位数）

直接根据公式代入得：

2^r-1 ≥ 4 + r

2^r-r ≥ 5

得到r最小为3

所以海明码的位数是4+3=7位

第二步：校验位和信息位对号入座

**注意： 信息位的位置分配是从高位到低位依次存放**

**注意： 海明校验码是放在2的幂次位上的**

![信息和校验码位置图](./images/1.png)

第三步：确定校验位的值

校验原则：被校验的海明位的下标等于所有参与校验该为的校验位的下标之和

![校验码校验位图](./images/2.png)

然后将校验码校验的信息位的位置记录下来：

* r1: 3, 5, 7
* r2: 3, 6, 7
* r3: 5, 6, 7

然后做对应信息位的异或运算(异或的运算法则为：0⊕0=0，1⊕0=1，0⊕1=1，1⊕1=0（同为0，异为1）)

* r1: 1 xor 1 xor 1 = 1
* r2: 1 xor 0 xor 1 = 0
* r3: 1 xor 0 xor 1 = 0

代入表格得到

![结果图](./images/3.png)

**注意：按照从低位到高位的排列顺序得到海明码：1010101**
