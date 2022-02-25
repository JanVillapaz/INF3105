# Scope

When declaring a program element such as a class, function, or a variable, its name can only be "seen" and used in certain parts of your program. The context in which a name is visible is called its *scope*.

Ex. If you declare a variable `x` within a function, `x` is only visible within that function body. 
It has local *scope*.

You may have other variables by the same name in your program; as long as they are in different scopes, they do not violate the One Definition Rule and no error is raised.

For automatic non-static variables, scope also determines when they are created and destroyed in program memory.

There are six kind of scope:

- **Global scope** A global name is one that is declared outside of any class, function, or namespace, in C++ even these names exist with an implicit global namespace.

The scope of global names extends from the point of declaration to the end of the file in which they are declared.

For global names, visibility is also governed by the rules of [linkage](https://docs.microsoft.com/en-us/cpp/cpp/program-and-linkage-cpp?view=msvc-170) which determine whether the name is visible in other files in he program.

- **Namespace scope** A name is declared within a [namespace](https://docs.microsoft.com/en-us/cpp/cpp/namespaces-cpp?view=msvc-170), outside of any class or enum definition or function block, is visible from its point of declaration
