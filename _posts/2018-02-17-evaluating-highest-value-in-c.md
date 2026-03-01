---
layout: post
title:  "Evaluating highest value of int in C language"
date:   2018-02-17 17:17:39 +0530
categories: 
---
In this lesson, we will see how we can evaluate the highest/lowest value of an **int** in C language. Unlike C++ and Java, this is not as straight forward as it may seem. To understand the value of the discussion below one should have a preliminary knowledge of 2's compliment arithmetic. 2's compliment arithmetic will not be discussed here. The general idea is this. 

Any numbers in a modern arithmetic is represented in 2's compliment form.  if a computer system is n bit wide then the highest number is $2^{n-1}-1$ and the lowest number is $2^{n-1}$.


Generally (not always), modern computers are 32 bit wide. So, highest positive number that **int** can represent or hold is $$2^{32-1}-1$  Similarly the lowest negative number representable in **int32** is $$2^{32-1}$.


Now, lets focus on representing this __highest positive number__ in C. That should be simple as given below:



```
int INT_MAX = (2^31)-1;

```
But this code, results into an overflow error. So what went wrong? To evaluate $(2^31)-1$, this is what the computer does: It takes the 1 and left shifts it by 31 bits.

```
00000000 00000000 00000000 00000001
```

on left shifting by 31 bits, we get
```
10000000 00000000 00000000 00000000
```

and now subtract -1 from it. -1 in 2s compliment form is
```
11111111 11111111 11111111 11111111
```
and now the following addition takes places
```
10000000 00000000 00000000 00000000
11111111 11111111 11111111 11111111
```

Now, clearly the addition above will result in a 33 bit number, hence a **overflow** .

Now to evaluate the expression $(2^31)-1$ correctly in C, we have to store the result in a data type bigger then 32 bits. For this, we use **long** data type.

```
long x = 1;
long INT_MAX = (x&amp;lt;&amp;lt;(sizeof(int)*8)-1)-1;

printf("%lu\n", INT_MAX); //outputs 2147483647 for 32 bit machine
```
