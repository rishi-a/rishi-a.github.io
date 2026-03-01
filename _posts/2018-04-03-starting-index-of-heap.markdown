---
layout: post
title:  "Prove that in a heap, the leaves starts from index ⌊n/2⌋+1,⌊n/2⌋+2,…,n"
date:   2018-04-3 17:17:39 +0530
categories: 
---

<p>We need to prove that in an array representation of heap, the leaves starts at index <strong>⌊n/2⌋+1</strong>, <strong>⌊n/2⌋+2</strong> . . .and goes till <strong>n</strong>, n being the last leaf of the heap.<br /><!--more--></p>
<p> </p>
<p>So, to prove it, first we recall that, the LEFT child and the RIGHT child of a node in a heap is given by:<br /> </p>
<pre>[code language="C"]
function LEFT(i){
    return 2i;
}
[/code]</pre>
<p> </p>
<pre>[code language="C"]
function RIGHT(i){
    return 2i+1;
}
[/code]</pre>
<p> </p>
<hr />
<p> </p>
<p> </p>
<p>Secondly, we also recall that, heaps are almost complete binary tree, meaning, we do not fill right child of any node without filling the left child first.</p>
<p> </p>
<hr />
<p> </p>
<p> </p>
<p>Third, realize the mathematical truth that, <strong>⌊n/2⌋ &gt; ( n/2 - 1 )</strong></p>
<hr />
<p>Now, we are good to go: Lets us take the index of the first leaf node, i.e <strong>⌊n/2⌋+1</strong>. For this node, we will attempt to find its left child:</p>
<p> <br /><code><br />
LEFT(⌊n/2⌋+1) = <span style="color: red;">2</span>(⌊n/2⌋+1)<br />
</code><br /> </p>
<p>Now:<br /><code><br />
<span style="color: red;">2</span>(⌊n/2⌋+1) &gt; [ 2( n/2-1 + 1) = 2n/2 - 2 + 2 = n ]<br />
</code></p>
<p> </p>
<p>Therefore:<br /><code><br />
LEFT(⌊n/2⌋+1) &gt; n<br />
</code><br />which is greater then the elements of the heap. Therefore ⌊n/2⌋+1 is a leaf and so is the next element, next to next element till n.</p>
<p> </p>