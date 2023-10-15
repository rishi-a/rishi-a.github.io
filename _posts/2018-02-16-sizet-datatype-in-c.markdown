---
layout: post
title:  "What is size_t data type in C and why is this important?"
date:   2018-02-16 17:17:39 +0530
categories: 
---
<p><strong>size_t</strong> data type is of equal importance just like any other data type. <strong>size_t</strong> represents size of an object. For example, if a function needs as parameter the size of <em>integer</em> or <em>character</em> then that size should be stored in<strong> size_t</strong> data type. <!--more-->In short, the return value of <strong>sizeof()</strong> should be stored in a variable of type <strong>size_t.</strong></p>
<p>Now the question is, <strong>Is unsigned int and size_t the same? Are they interchangeable?</strong></p>
<p><strong>No, </strong>the code below explains why.</p>
<pre>[code language="C"]

unsigned int size1&amp;amp;nbsp; = sizeof(int); //this is valid

size_t size2 = sizeof(int); //this is also valid

unsigned int size3 = sizeof(char); //ERROR, this is obviously wrong

size_t size4 = sizeof(char); //this is valid

[/code]</pre>
<p> </p>
<p>So, you got the difference now? <strong>size_t</strong> can hold size of any type of any data type. <strong>unsigned int</strong> can hold size of <em>integer</em> only.  We should not have had this doubt at the first place.</p>
<p> </p>
<p>This knowledge will help us in understanding about creating linked list which can hold any data type.</p>