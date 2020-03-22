# c_plus_plus_notes
Pointers:
         Pointers as its name suggest are pointing to some memory location of some variable. This variable can be of primary type or any custom type. As they store memory address where the variable is stored.
         
Good:
     No need to copy memory contains from calling function to called function to pass input or get output.

Risk:
     Memory management is required to allocate and free the memory.
     Incrementing or decrementing pointer could make application behave unexpected.
 
Smart Pointer:
     use of new don't handle exceptions hence not recommended.
     No need of explicit freeing of the memory.
     a. Unique Pointer: only one copy created of the pointer, can not assign/copy. hence Unique. ownership is only with one.
     b. Shared Pinter: These pointers can be shared, (assign copy operations work/ owned by many). We can pass one one shared pointer to another function. Memory will be free when all scopes of uses where it is shared exited. Shared counter(use_count) will be stored as meta information of the pointer, when the same pointer shared with other the counter gets increamented, when one of scope where it is shared exited counter gets decremented.
     c. Weak pointer: same as shared only counter is not maintained. Shared pointer and weak pointers can be assigned to each other. Hence if we have all scopes of shared pointers exited and if some weak pointer is still in the scope then it can result in pointing to memory location which is not valid(null_ptr). Hence expired() is used to check whether the pointer is still valid or not.
