# nettyholdspringmvc
show how to run springmvc with netty


see
[me](http://blog.csdn.net/imlsz/article/details/42673507)

JAVA中Boolean占几个字节
https://blog.csdn.net/xb113338l2/article/details/82532315
java规范中，没有明确指出boolean的大小。在《Java虚拟机规范》给出了4个字节，和boolean数组1个字节的定义，具体还要看虚拟机实现是否按照规范来，所以1个字节、4个字节都是有可能的

弄清java中的字节与字符
https://blog.csdn.net/u012501054/article/details/81094300
问题
在java中，一个字符等于多少字节？或者更详细的问：在java中，一个英文字符等于多少字节？一个中文字符等于多少字节？ 
答案
Java采用unicode来表示字符，java中的一个char是2个字节，一个中文或英文字符的unicode编码都占2个字节，但如果采用其他编码方式，一个字符占用的字节数则各不相同。
在 GB 2312 编码或 GBK 编码中，一个英文字母字符存储需要1个字节，一个汉子字符存储需要2个字节。
在UTF-8编码中，一个英文字母字符存储需要1个字节，一个汉字字符储存需要3到4个字节。
在UTF-16编码中，一个英文字母字符存储需要2个字节，一个汉字字符储存需要3到4个字节（Unicode扩展区的一些汉字存储需要4个字节）。
在UTF-32编码中，世界上任何字符的存储都需要4个字节。


java中String最大多少？
String内部使用char[]存储数据。允许的长度是固定的，因为char的元素是由下标来定位的，而下标的类型为int，所以char最多只能表示2^31 - 1，也就是说string可以表示的长度为2^31 - 1，由于char占用两个字节，所以所占空间还要*2. 所以string的长度只能为2^32 - 1。

为什么正数要减一？
32位int 
正数（符号位是0）：0~2147483647
负数（符号位是1）：-1~2147483648
正负都是2147483648个（2的31次方） 只不过0放到正数（符号位为0）那边
