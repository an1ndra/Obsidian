The `@Nullable` annotation helps you detect:

-   Method calls that can return null
    
-   Variables (fields, local variables, and parameters), that can be null
    

Methods with the `@Nullable` annotation in the parent method can have either `@Nullable` or `@NotNull` annotations in the child class method.

The `@Nullable` annotation of the parameter in the parent method requires the `@Nullable` annotation in the child class method parameter.