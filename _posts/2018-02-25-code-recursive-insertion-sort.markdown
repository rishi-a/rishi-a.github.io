---
layout: post
title:  "Program Code For Recursive Insertion Sort"
date:   2018-02-25 17:17:39 +0530
categories: 
---

<p>Iterative insertion sort is very common. In this post, the recursive insertion sort is given. <!--more--></p>
<pre>[code language="C"]
void recursiveInsertionSort(int *a, int k, int key){

	if(k&amp;lt;0){		//if index is &amp;lt;0 which means indexes are over
		a[0] = key;
		return;
	}

	if(a[k] &amp;gt; key){
		a[k+1] = a[k];
		recursiveInsertionSort(a, k-1, key);
		return;
	}
	else{
		a[k+1] = key;
		return;
	}

}

[/code]</pre>
<p> </p>
<p>I would encourage you to write the driver program yourself by understanding the recursiveInsertionSort() function implementation. A hint is given below.</p>
<p> </p>
<pre>[code language="C"]
...
for(i=1; i&amp;lt;n; i++){ 		//i is the index of array | a[i] is the Key
		k = i - 1;
		recursiveInsertionSort(a, k, a[i]); //args: array | index | key
	}

...
[/code]</pre>

