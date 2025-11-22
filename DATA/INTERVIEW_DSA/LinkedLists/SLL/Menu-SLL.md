
1. INTRO
	 1.  [[SLL-Basics]]
	 2. [[Big-O]]
	 3. [[SLL-Representation]]
	 4.  [[code for SLL]]
2. Operations
	1. [[SLL-PRINT]]
	2. [[SLL-APPEND]]
	3. [[SLL-POP LAST]]
	4. [[SLL-PREPEND]]
	5. [[SLL-POP-FIRST]]
	6. [[SLL-GET]]
	7. [[SLL-SET]]
	8. [[SLL-INSERT]]
	
---


| Sl. no. | Operation  | Cases              | Pointers                      | Note                                                                                    |
| ------- | ---------- | ------------------ | ----------------------------- | --------------------------------------------------------------------------------------- |
| 1       | *printing* | same for all cases | 1. temp                       | - temp variable to translate and print                                                  |
| 2       | *append*   | 1. empty           | 0. None                       | - checking head is none and then pointing head and tail to new node                     |
|         |            | 2. normal          | 0. None                       | - make tail point to new node and make new node the tail                                |
| 3       | *pop*      | 1. empty           | 0. None                       | - return none - check for length or head                                                |
|         |            | 2. only one        | 0. None                       | - either check at last or check for length==1 and return head                           |
|         |            | 3. normal          | two pointers - 1. temp 2. pre | - two pointers - temp and pre. temp moves in front. when temp.next == None - pop - pre. |
| 4       | prepend    | 1. empty           | 0. None                       | - if length = 0 , make new node  = head , tail                                          |
|         |            | 2. normal          | 0. None                       | - make new node point to head and make new node as head                                 |
|         |            |                    |                               |                                                                                         |
|         |            |                    |                               |                                                                                         |
|         |            |                    |                               |                                                                                         |
|         |            |                    |                               |                                                                                         |
