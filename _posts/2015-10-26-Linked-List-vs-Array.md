---
layout: post
category : Algorithms
tagline: ""
tags : [Algorithms]
---
{% include JB/setup %}

# Linked List vs. Array

- Its much easier to add elements to a linked list. Arrays size must be known or it will be recreated when new elements are added.
- Arrays assume each element in the array is the same size. This makes it advantageous to use a linked list if each element will have varying sizes
- Shuffleing a linked list is much more efficient than an array, you simply change the pointers. Shuffling an array takes more memory
- Linked lists are also superior in multi-threaded implementations. Two processes can be occurring on a linked list at once.
- A VECTOR CONTAINER IS A TYPE OF DYNAMIC ARRAY THAT WILL SHRINK AND EXPAND AUTOMATICALLY. THEY ALSO PROVIDE CONSTANT TIME TO ELEMENTS WITHIN THE CONTAINER VIA INDEX - JUST LIKE AN ARRAY. WHEN THE VECTOR NEEDS TO ADD MORE SPACE FOR ADDITIONAL ELEMENTS IT TYPICALLY DOUBLES IN SIZE
- From wikipedia:
Linked lists have several advantages over arrays. Elements can be inserted into linked lists indefinitely, while an array will eventually either fill up or need to be resized, an expensive operation that may not even be possible if memory is fragmented. Similarly, an array from which many elements are removed may become wastefully empty or need to be made smaller.
On the other hand, arrays allow random access, while linked lists allow only sequential access to elements. Singly-linked lists, in fact, can only be traversed in one direction. This makes linked lists unsuitable for applications where it's useful to look up an element by its index quickly, such as heapsort. Sequential access on arrays is also faster than on linked lists on many machines due to locality of reference and data caches. Linked lists receive almost no benefit from the cache.
Another disadvantage of linked lists is the extra storage needed for references, which often makes them impractical for lists of small data items such as characters or boolean values. It can also be slow, and with a naïve allocator, wasteful, to allocate memory separately for each new element, a problem generally solved using memory pools.

- Concatenating multiple linked lists, you can simply point one to another, so combining them is constant O(1) time. However with arrays this will take O(n) time.
- In a language like Ruby its typically more practical, especially for debugging purposes to use an Array over a Linked List.
- CONTIGUOUS MEMEORY SPACE IS MEMEORY ALLOCATED WITHOUT GAPS OR ALL OF ONE BLOCK. NON-CONTIGUOUS IS FRAGMENTED MEMORY
- Arrays have better caching because they occupy contiguous memory space


Standard dynamic array:

operation|worst|
---------|-----|
`[]`|O(1)
`[]=`|O(1)
`push`|O(n)
`pop`|O(1)
`shift`|O(n)
`unshift`|O(n)

