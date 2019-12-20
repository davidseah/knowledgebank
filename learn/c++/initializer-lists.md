# Initializer Lists

When we want to initialize a vector, we had to do the following

```cpp
//c++03
std::vector v;
v.push_back(1);
v.push_back(2);
v.push_back(3);
v.push_back(4);
```

Now, with c++11, we can do this:

```cpp
//c++11
std::vector v = { 1, 2, 3, 4 };
```



