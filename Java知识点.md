# java

## split分割 任意数量的空格  制表符  "\\s+"


id userName sex
0  root     male
1  user1    female
我要从上述文件读取每一行字符串并且split，但是由于格式化以及各人之间的习惯，每一行中间都充斥着空格和Tab键，因此第一种解决方案无法运用到这上面去。想到正则表达式中有“\s”代表任意空白字符，这里便可以解决问题：
   

```java
String sample1 = "0  root       male";
String sample2 = "1  user1  female";
String[] arrays = sample1.split("\\s+");
for(String s : arrays)
{
    System.out.println(s);
}
System.out.println("----------------------");
arrays = sample2.split("\\s+");
for(String s : arrays)
{
    System.out.println(s);
}
```
