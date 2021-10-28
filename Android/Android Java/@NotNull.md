The `@NotNull` annotation is, actually, an explicit contract declaring that:

-   A method should not return null
    
-   Variables (fields, local variables, and parameters) cannot hold a null value
    

IntelliJ IDEA warns you if these contracts are violated.

The `@NotNull` annotation of the parent method requires the `@NotNull` annotation for the child class method.

Methods with the `@NotNull` annotation of the parameter in the parent method can have either `@Nullable` or `@NotNull` annotations (or none of them) in the child class method parameter.