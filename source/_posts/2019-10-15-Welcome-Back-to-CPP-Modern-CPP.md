---
title: Welcome Back to C++ (Modern C++)
date: 2019-10-15 10:28:21
categories:
tags: C++ C
---

<https://docs.microsoft.com/zh-tw/cpp/cpp/welcome-back-to-cpp-modern-cpp>


<https://stackoverflow.com/a/9338032>

1. Final Class: C++11 provides the final specifier to prevent class derivation

2. C++11 lambdas substantially reduce the need for named function object (functor) classes.

3. Move Constructor: The magical ways in which std::auto_ptr works are no longer needed due to first-class support for rvalue references.

4. Safe bool: This was mentioned earlier. Explicit operators of C++11 obviate this very common C++03 idiom.

5. Shrink-to-fit: Many C++11 STL containers provide a shrink_to_fit() member function, which should eliminate the need swapping with a temporary.

6. Temporary Base Class: Some old C++ libraries use this rather complex idiom. With move semantics it's no longer needed.

7. Type Safe Enum Enumerations are very safe in C++11.

8. Prohibiting heap allocation: The = delete syntax is a much more direct way of saying that a particular functionality is explicitly denied. This is applicable to preventing heap allocation (i.e., =delete for member operator new), preventing copies, assignment, etc.

9. Templated typedef: Alias templates in C++11 reduce the need for simple templated typedefs. However, complex type generators still need meta functions.

10. Some numerical compile-time computations, such as Fibonacci can be easily replaced using generalized constant expressions

11. result_of: Uses of class template result_of should be replaced with decltype. I think result_of uses decltype when it is available.

12. In-class member initializers save typing for default initialization of non-static members with default values.

13. In new C++11 code NULL should be redefined as nullptr, but see STL's talk to learn why they decided against it.

14. Expression template fanatics are delighted to have the trailing return type function syntax in C++11. No more 30-line long return types!