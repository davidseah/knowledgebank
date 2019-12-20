# Initializer Lists

When we want to initialize a vector, we had to do the following

```cpp
//C++03
std::vector v;
v.push_back(1);
v.push_back(2);
v.push_back(3);
v.push_back(4);
```

Now, with C++11, we can do this:

```cpp
//c++11
std::vector v = { 1, 2, 3, 4 };
```

C++11 binds the concept to a template, called std::initializer\_list. This allows constructors and other functions to take initializer-lists as parameters.

```cpp
#include <iostream>
#include <vector>

class MyNumber
{
    public:
    MyNumber(const std::initializer_list<int> &v)
    {
        for( auto itm : v)
        {
            mVec.push_back(itm);
        }
    }
    
    void Print()
    {
        for(auto itm : mVec)
        {
            std::cout << itm << " ";
        }
    }
    
    private:
    std::vector<int> mVec;    
};


int main()
{
    MyNumber m = {1,2,3,4,5};
    m.Print();

    return 0;
}
```

[code on Wandbox](https://wandbox.org/permlink/UoPQ5m1t644yAcgu)

