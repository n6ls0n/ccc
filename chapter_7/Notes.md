# Chapter 7 Notes

- Both **const** and **constexpr** are closely related. Whereas **constexpr** enforces that an expression is compile time evaluable, const enforces that a variable cannot change within some scope (at runtime). All **constexpr** expressions are const because they’re always fixed at runtime.

- Using **constexpr** rather than manually calculated literals can make your code more expressive. Often, it can also seriously boost performance and safety at runtime. This means access cannot be optimized out or reordered with another visible side effect.

- The **volatile** keyword tells the compiler that every access made through this expression must be treated as a visible side effect. This means access cannot be optimized out or reordered with another visible side effect.
