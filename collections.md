## Q1ArrayList vs LinkedList
+ ArrayList -> Fast read, slow insert/delet
+ LinkedList -> Fast insert/delete, slow random access

## Q2 HashMap vs HashSet?
+ HashMap -> Key-Value
+ HasSet -> Only values (internally uses HashMap)

## Q3 How does HashMap work internally?
**Answer** 
+ Hash Key
+ Find bucket
+ Store as Node
+ Collision -> LinkedList -> Red Black Tree

## Q4 Why Hashmap is not thread safe?
**Answer** No synchronization
Concurrent updates -> data inconsistency

## Q5 HashMap vs ConcurrentHashMap
**Answer**
+ Concurrent HashMap:
  + Thread-safe
  + Uses bucket-level locking
  + No full map lock
  
## Q6 Why HashMap allows one null key?
**Answer** Because only one hash bucket can represent null

## Q7 Trremap vs HashMap
**Answer**
+ Treemap -> Sorted (Red-black tree)
+ HashMap -> Unordered

## Q8 Fail-fast vs Fail-Safe
**Answer** 
+ Fail-fast -> Throws ConcurrentModificationException
+ Fail-Safe -> Works on copy, no exception 