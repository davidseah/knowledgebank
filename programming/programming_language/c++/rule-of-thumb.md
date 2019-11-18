# Rule of Thumb

### Initialization List

Always use initialization list for plain old data. 

[https://daemons.net/programming/c++/initialization.html](https://daemons.net/programming/c++/initialization.html)

{% embed url="https://daemons.net/programming/c++/initialization.html" %}

{% embed url="http://mikelui.io/2019/01/03/seriously-bonkers.html" %}

{% embed url="http://scottmeyers.blogspot.com/2015/09/thoughts-on-vagaries-of-c-initialization.html" %}

```cpp

```

## Virtual Table and Virtual Pointer

The way compilers handle virtual functions is to add a hidden member to each object. The hidden member holds a pointer to an array of function addresses. Such an array is usually termed a **virtual function table\(vtbl\)**. The vtbl holds the addresses of the virtual functions declared for objects of that class.

An object of a base class, for example, contains a pointer to a table of addresses of all the virtual functions for that class. An object of a derived class contains a pointer to a separate table of addresses. If the derived class provides a new definition of a virtual function, the **vtbl** holds the address of the new function. If the derived class doesn't redefine the virtual function, the **vtbl** holds the address of the original version of the function. If the derived class defines a new function and makes it virtual, its address is added to the **vtbl**. So, whether we define 1 or 100 virtual functions for a class, we are adding just one address member to an object.

When we call a virtual function, the program looks at the **vtbl** address stored in an object and goes to the corresponding table of function addresses. If we use the first virtual function defined in the class declaration, the program uses the first function address in the array and execute the function that has that address, and so on.

1. Each object has its size increased by the amount needed to hold that address.
2. For each class, the compiler creates a table of addresses of virtual functions.
3. For each function call, there's an extra step of going to a table to look up an address.

In summary, virtual functions are implemented using a table of function pointers, called the vtable. There is one entry in the table per virtual function in the class. **This table is created by the constructor** of the class. When a derived class is constructed, its base class is constructed first which creates the vtable. If the derived class overrides any of the base classes virtual functions, those entries in the vtable are overwritten by the derived class constructor. This is why you should never call virtual functions from a constructor, and that's because the vtable entries for the object may not have been set up by the derived class constructor yet, so you might end up calling base class implementations of those virtual functions

Taken from [https://www.bogotobogo.com/cplusplus/slicing.php](https://www.bogotobogo.com/cplusplus/slicing.php).

  


