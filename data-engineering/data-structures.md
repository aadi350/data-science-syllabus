# Hash Tables  
Keeps track of evolving set of objects indexed via keys

## Supported Operations  

**Lookup**(a.k.a. Search): for a key k, return a pointer to an object in the hash table with key k (or report that no such object exists)  
**Insert**: given a new object x, add x to the hash table.  
**Delete**: for a key k, delete an object with key k from the hash table, if one exists.

### Hash Functions  
*Defines how keys are mapped to positions in an array*  
A good hash function must be:
- cheap to evaluate, ideally in constant time
- easy to store, ideally with constant memory
- some random functoin spreading out non-pathological data sets roughly evenly across positions. 

#### For Primitive Data Types  
*char, byte, int, float*  
Treat the bits as representation of an integer  

#### For Compound Objects 
Combines each individual hash codes of the constituent parts.  

#### For Strings  
Based on a polynomial over a prime field (evaluated modulo against some prime number *p*)

### Collision Resolution
#### Separate Chaining 
Stores a linked-list for multiple objects hashed to the same position (index). Lookup times degrade if the hash table becomes heavily populated or if the hash function results in too many collisions.
#### Open Addressing
Easier to implement than chaining (except in the $DELETE$ operation's case). Each position stores a $0$ or $1$. Each key is associated with a probe-sequence of positions (first, second, third, etc..) to suggest new positions when collisions occur. 

**Linear Probing**: new position in probe sequence is constant from last tried position.  
**Double Hashing**: two hash functions, first gives normal index position, second indicates offset.


## <div style="color:#0A0">Advantages</div> 
- Constant-time *lookups* (searches), insert and delete

## <div style="color:#A00">Disadvantages</div> 
- Cannot perform range-queries  
- Must be kept in memory


# Binary Trees  

# B-Trees

# Bloom Filters  

# Linked List  
