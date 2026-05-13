
1. **INTRODUCTION**

	 1.  [[SLL-Basics]]
	 2. [[Big-O]]
	 3. [[SLL-Representation]]
	 4.  [[code for SLL]]

2. 

| Sl. no. | Operation     | Cases                 | Pointers              | Note                                                                                    | Link              |
| ------- | ------------- | --------------------- | --------------------- | --------------------------------------------------------------------------------------- | ----------------- |
| 1       | **PRINT**     | 1. normal             | 1: temp               | - temp variable to translate and print                                                  | [[SLL-PRINT]]     |
| 2       | **APPEND**    | 1. empty              | 0: None               | - checking head is none and then pointing head and tail to new node                     | [[SLL-APPEND]]    |
|         |               | 2. normal             | 0. None               | - make tail point to new node and make new node the tail                                |                   |
| 3       | **POP**       | 1. empty              | 0. None               | - return none - check for length or head                                                | [[SLL-POP LAST]]  |
|         |               | 2. only one           | 0. None               | - either check at last or check for length==1 and return head                           |                   |
|         |               | 3. normal             | 2 :  1. temp,  2. pre | - two pointers - temp and pre. temp moves in front. when temp.next == None - pop - pre. |                   |
| 4       | **PREPEND**   | 1. empty              | 0. None               | - if length = 0 , make new node  = head , tail                                          | [[SLL-PREPEND]]   |
|         |               | 2. normal             | 0. None               | - make new node point to head and make new node as head                                 |                   |
| 5       | **POP FIRST** | 1. empty              | 0. None               | -  check for length == 0                                                                | [[SLL-POP-FIRST]] |
|         |               | 2. only one           | 0. None               | - to change tail== none                                                                 |                   |
|         |               | 3.Normal              | 1: temp               | - make head to temp , then move head to next value and then return temp                 |                   |
| 6       | **GET**       | 1. index out of range | 1: temp               | - getting the value at particular index . - translate to the index and return the node. | [[SLL-GET]]       |
| 7       | **SET**       | 1. index out of range | 1: temp               | - use GET method. - If no Node is returned - edge case                                  | [[SLL-SET]]       |
| 8       | **INSERT**    | 1. PREPEND            |                       | - use PREPEND to insert at begining                                                     | [[SLL-INSERT]]    |
|         |               | 2. APPEND             |                       | - use APPEND to insert at the end                                                       |                   |
|         |               | 3. NORMAL             | 1: temp               | - use temp to translate and then reassign the nodes                                     |                   |

   
	
	