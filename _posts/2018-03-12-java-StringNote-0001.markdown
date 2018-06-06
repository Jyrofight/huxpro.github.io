---
layout:     post
title:      "java核心技术卷一学习笔记（一）字符串类"
subtitle:   " \"Hello World, Hello Java\""
date:       2018-03-12 19:00:00
author:     "JyRo"

catalog: true
tags:
    - Java 
---

### Leading

概念上讲，JAVA字符串是UNICODE字符序列。<br/>
<i>Concepttually,Java strings are sequences of Unicode characters.</i><br /><br />
Java没有内置的字符串类型，而在标准java类库中提供了一个<u>预定义类</u>。<br/>
<i>Java does not have a built-in string type.Instead, the standard Java library contains a predefined class called String.</i>
<br /><br />
每个用双引号括起来的字符串就是String的一个实例。<br />
<i>Each quoted string is an instance of the String class.</i>

---

### 1.Strings Are Immutable  不可变字符串 ###
The String class give no methods to change a character in an existing string.  
A java string is roughly analogous to a char* pointer，instead of arrays of characters.<br/>
Java字符串更像char*指针，而不是字符串数组。
<br/>
PS：概念相关：变量-对象-对象的引用

---

### 2.Testing Strings for Equality ###
	s.equals(t)
	s.equalsIgnoreCase(t)
<p>
“==” 只是用来确认是否放在同一个位置。若位置相同，自然相等。但相同内容的字符串的靠背可能放置在不同的位置上。<br/>
<i>  operator "==" only determines whether or not two strings are stored in the same location. </i>
</p>
---
### 3.空串与Null串 ###
空串("")是一个Java对象，有自己的串长度（0）和内容（空）。<br />
NULL表示暂未有对象与变量相关联。

	if(str == null)
	if(str ！=null &&str.length()!=0)

第二行用于检查一个字符串既不是NULL也不是空串。
<br>PS：NULL上不能调用方法，首先查是否是NULL串。

---
### 4.StringBuffer/StringBuilder ###

<i>It would be inefficient to use string concatenation for string combining.</i>

采用字符串类连接（“+”）的方式来构建字符串的效率比较低。所以引入StringBuilder类。

	StringBuilder builder = new StringBulier();

append方法。

	builder.append(ch);//a single character 
	builder.append(str);//a string

---
### 5.常用API ###

略。

---

## Java字符串到此结束。 ##


