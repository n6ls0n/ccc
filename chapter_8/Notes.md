# Chapter 8 Notes

- Functions that aren’t member functions are called non-member functions, or sometimes free functions, and they’re always declared outside of main() at namespace scope. A function definition includes the function declaration as well as the function’s body. A function’s declaration defines a function’s interface, whereas a function’s definition defines its implementation.

- "::" -> scope resolution operator. This can be used to access members of a namespace such as in Namespace::Member. It can also be used to access members of an enum such as Enum::Member and should the enum have been defined withing a namespace the result is Namespace::Enum::Member

- You can employ a using directive to avoid a lot of typing. A using directive imports a symbol into a block or, if you declare a using directive at namespace scope, into the current namespace.

- With a "using namespace" directive, you can use classes, enum classes, functions, and so on within your program without having to type fully qualified names. Of course, you need to be very careful about clobbering existing types in the global namespace. Usually, it’s a bad idea to have too many using namespace directives appear in a single translation unit.

- You should never put a "using namespace" directive within a header file. Every source file that includes your header will dump all the symbols from that "using directive" into the global namespace. This can cause issues that are very difficult to debug.

- A type alias defines a name that refers to a previously defined name. You can use a type alias as a synonym for the existing type name.
To declare a type alias, you use the following format, where type-alias is the type alias name and type-id is the target type: "using type-alias = type-id;"

- On using the keyword static on a variable. **File Scope**: "static" variables declared outside of any function have file scope, not global scope. They are accessible throughout the file they're declared in, but not in other files. **Internal Linkage**: "static" gives the variable internal linkage. This means the variable is only visible within its translation unit. **Translation Unit**: A translation unit is the source file being compiled, along with all its included header files. **Lifetime**: The variable has static storage duration, existing for the entire run of the program. **Initialization**: It's initialized when the program starts, before main() is called. **No External Linkage**: Other translation units cannot access this variable, even with an extern declaration. **Name Collision Prevention**: Helps prevent name collisions with variables in other translation units.

- Structured bindings enable you to unpack objects into their constituent elements.

- Attributes apply implementation-defined features to an expression statement. eg. [[noreturn]]

- You can make an if statement constexpr; such statements are known as constexpr if statements. A constexpr if statement is evaluated at compile time. Code blocks that correspond to true conditions get emitted, and the rest is ignored.
