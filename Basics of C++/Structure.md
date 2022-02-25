# Using namespace std

You may have seen `cout` instead of `std::cout`. 

Both name the same object: 
- The first one uses its *unqualified name* (`cout`).
- The second one qualifies it directly within the *namespace* `std` (`std::cout`)


`cout` is part of the standard library, and all the elements in the standard C++ library are declared within what is called a *namespace*: the namespace `std`.

In order to refer to the elements in the `std` namespace a program shall either qualify each and every use of elements of the library (as we have done by prefixing `cout` with `std::`), or introduce visibility of its components. The most typical way to introduce visibility of these components is by means of *using declarations:*

```c++
using namespace std;
```

The above declaration allows all elements in the `std` namespace to be accessed in an *unqualified* manner (without the `std::` prefix)

Code:
```c++
// my second program in C++
#include <iostream>
using namespace std;

int main ()
{
  cout << "Hello World! ";
  cout << "I'm a C++ program";
}
```

Output:
```console
Hello World! I'm a C++ program
```

Both ways of accessing the elements of the `std` namespace (explicit qualification and *using* declarations) are valid in C++ and produce the exact same behavior. For simplicity, and to improve readability.

*Explicit qualification* is the only way to guarantee that name collisions never happen.
