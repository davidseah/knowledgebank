# Unique Pointer

Manages the storage of a pointer, providing a limited garbage-collection facility, with little to no overhead over built - in pointer\(depending on the deleter used\).

These objects have the ability to taking ownership of a pointer: once they take ownership they manage the pointed object by becoming responsible for its deletion at some point. 

unique\_ptr objects automatically delete the object they manage \(using a deleter\) as soon as they themselves are destroyed, or as soon as their value changes wither by an assignment or by an explicit call to unique\_ptr::reset.

unique\_ptr object own their pointer uniquely: no other facility shall take care of deleting the object, and this no other managed pointer should point to its managed object, since as soon as they have to, unique\_ptr objects delete their managed object without taking into account whether other pointers still point to the same object or not, and thus leaving any other pointers that point there as pointing to an invalid location. 

A unique\_ptr object has two components:

* a stored pointer: the pointer to the object it manages. This is set on construction, can be altered by an assignment operation or by calling member reset, and can be individually accessed for reading using members get or release.
* a stored deleter: a callable object that takes an argument of the same type as the stored pointer and is called to delete the managed object. It is set on construction, can be altered by an assignment operation, and can be individually accessed using member get\_deleter.



