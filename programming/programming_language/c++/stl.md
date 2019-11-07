# Overview

## Class

Rule of thumb when creating class

1. [Rules of Big 5](https://www.feabhas.com/sites/default/files/2016-06/Rule%20of%20the%20Big%20Five.pdf)
   1. destructor
   2. assignment operator
   3. copy constructor
   4. move constructor
   5. move assignment operator

```cpp
class Complex{    public:    Complex(int r, int i):    real(r),     imagine(i)    {}    Complex() :    real (0),     imagine (0)    {}        void Print()    {        std::cout << "real: " << real << " imagine: " << imagine << "\n";    }    private:    int real, imagine;};
```

[View Code on Wandbox](https://wandbox.org/permlink/FXsl1iY4GIDZ7FpE)

## Operator overload

```cpp
#include <iostream>class Complex{    public:    Complex(int r, int i):    real(r),     imagine(i)    {}    Complex() :    real (0),     imagine (0)    {}        void Print()    {        std::cout << "real: " << real << " imagine: " << imagine << "\n";    }        //copy constructor    Complex(const Complex& rhs)    {        real = rhs.real;        imagine = rhs.imagine;    }    //overload operator +    Complex operator + (const Complex& rhs)    {        Complex res;        res.real = real + rhs.real;        res.imagine = imagine + rhs.imagine;        return res;    }        //overload operator -    Complex operator - (const Complex& rhs)    {        Complex res;        res.real = real - rhs.real;        res.imagine = imagine - rhs.imagine;        return res;    }        //overload operator =    void operator = (const Complex& rhs)    {        real = rhs.real;        imagine = rhs.imagine;    }        //overload operator <<        //destructor    ~Complex()    {    }    private:    int real, imagine;};
```

[View Code on Wandbox](https://wandbox.org/permlink/erqOQ01s57XPO9rP)

