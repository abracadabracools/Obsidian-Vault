[[code for LL]]
---
1 - Print
 - create a new pointer and translate with it to next nodes

![[Pasted image 20251029065957.png]]

---
2 - Append - Use tail to easily append at the end

 - two cases 
	 - case - 1 - Empty list
	 - case - 2 - Normal List - Update Tail

![[Pasted image 20251029073424.png]]

---

3 - Pop (Last)
- Cases
	- Empty List
	
	 ![[Pasted image 20251107085140.png]]
	
	- Normal List 
		- Two pointers to translate
		

![[Pasted image 20251107085317.png]]

- Translation 

![[Pasted image 20251107085458.png]]

 - End of two pointer translation

![[Pasted image 20251107085555.png]]

- code 
![[Pasted image 20251107091458.png]]

- CASE-3 - Only one Node

	- ![[Pasted image 20251107091602.png]]

 - FINAL CODE
		![[Pasted image 20251107091650.png]]

---

==PREPEND==

- Add a new Node at the beginning

![[Pasted image 20251107091944.png]]

Cases -

- Empty case

	![[Pasted image 20251107092120.png]]

- Normal case
  - Join new Node to list
  - update head to new node
![[Pasted image 20251107092215.png]]

---
