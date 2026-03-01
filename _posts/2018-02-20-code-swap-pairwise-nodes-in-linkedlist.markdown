---
layout: post
title:  "Swap all pairwise nodes in a linked list"
date:   2018-02-20 17:17:39 +0530
categories: 
---
<p>In this lesson, I will show you an iterative program to swap all pairwise nodes of a linked list.<!--more--></p>
<p><strong>Are we swapping the pairwise data of nodes or the complete node?</strong><br /> </p>
<p>We'll we swapping the nodes, as a result the data will get swapped. Swapping only the element does not make any sense.</p>
<p> </p>
<p>For example, if the linked list is 1-2-3-4-5-6 then pairwise swapping all nodes will give us the linked list 2-1-4-3-6-5.</p>
<p> </p>
<p>If the linked list is 1-2-3-4-5 then pairwise swapping all nodes will give us the linked list 2-1-4-3-5.</p>
<p> </p>
<p><img class="" src="/images/pairwise-swap-LL.png" alt="" width="463" height="261"/></p>
<p> </p>
<p>Observe the representation above, the address and data of the nodes.</p>
<p> </p>
<p>The following program code require the understanding of <strong>insertAfter()</strong> function and <strong>printList()</strong> function.</p>
<p> </p>
<pre>[code language="C"]
/Pairwise swap all elements of linked list.

#include&amp;amp;lt;stdio.h&amp;amp;gt;
#include&amp;amp;lt;stdlib.h&amp;amp;gt;

struct Node{
	int data;
	struct Node *next;
};

void printList(struct Node*);
struct Node* insertAfter(struct Node**, int); //returns adress of last node
void pairWiseSwap(struct Node**);

int main()
{
	struct Node *head;
	struct Node *endMarker;
	head = (struct Node*)malloc(sizeof(struct Node));
	head-&amp;amp;gt;data = 1;
	head-&amp;amp;gt;next = NULL;
	endMarker = insertAfter(&amp;amp;amp;head, 2);
	endMarker = insertAfter(&amp;amp;amp;endMarker, 3);
	endMarker = insertAfter(&amp;amp;amp;endMarker, 4);
	endMarker = insertAfter(&amp;amp;amp;endMarker, 5);
	endMarker = insertAfter(&amp;amp;amp;endMarker, 6);

	pairWiseSwap(&amp;amp;amp;head);

	printList(head);

	return 0;
}

void pairWiseSwap(struct Node **head){
	struct Node *t1, *t2, *beforeT1 = NULL;
	int count = 0;

	//init
	t1 = *head;
	t2 = (*head)-&amp;amp;gt;next;

	while(t1 &amp;amp;amp;&amp;amp;amp; t2){

		t1-&amp;amp;gt;next = t2-&amp;amp;gt;next;
		t2-&amp;amp;gt;next = t1;

		if(count == 0)
			(*head) = t2;
		else{
			beforeT1-&amp;amp;gt;next = t2;
		}

		beforeT1 = t2;

		if(t2-&amp;amp;gt;next == NULL)
			t1 = NULL;
		else
			t1 = t1-&amp;amp;gt;next; //t1 = t1-&amp;amp;gt;next;

		if(t1 == NULL)
			t2 = NULL;
		else
			t2 = t1-&amp;amp;gt;next;

		count++;
		beforeT1 = beforeT1-&amp;amp;gt;next;
	}

}

void printList(struct Node* node){
	int count=0;
	while(node!=NULL){
		printf("\t%d", node-&amp;amp;gt;data);
		node = node-&amp;amp;gt;next;
		count++;
	}
	printf("\nTotal nodes printed=\t%d\n", count);
}

struct Node* insertAfter(struct Node **node, int data){
    if( (*node)==NULL) {
        printf("Node Does Not Exists\n");
        return NULL;
    }
    struct Node *new = (struct Node*)malloc(sizeof(struct Node));
    new-&amp;amp;gt;data = data;
    new-&amp;amp;gt;next = (*node)-&amp;amp;gt;next;
    (*node)-&amp;amp;gt;next = new;
    return new;
}

[/code]</pre>
