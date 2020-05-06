The granite project is about secure java programming.

There are two intended users of this work:
1. Those who simply want to use secure software.
2. Those who want to create secure software.

Here is the nightmare scenario that combines many elements of
insecure coding practices:

You have code running on the production server and you get a zero-day CVE vulnerability
in a library that is used by a library you are using directly.
First you have to wait for a new version of the library you are using to be published.
Then you have to drop what you are doing, use the new version and send it through your development cycle.
This cycle can be very lengthy, and costly, expecially when you are using an older (perhaps no longer supported) version
of the vendor's code.

So what could have been done differently?

100% backwards compatibility:
It should be that you can do a direct replacement of the sub vendor's code when they make a fix
available, and use it knowing it fully fulfilled the functionality of the old code.

Avoiding code bloat:
The larger your code, the larger the probability of a problem at any given time.
Perhaps the code that had a CVE was never, actually, used by your product at all.

Although nothing can guarantee your java code is secure, by adopting
a few small guidelines, you can help ease your security, portability, and usefulness.

Here are the hallmarks of the "Granite Seal of Approval"

1. No use of any external libraries that do not have the "Granite Seal of Approval"
2. 100% backwards compatibility with previous version of your product
3. Small Size
4. Targeted Scope
5. Copious Testing
6. 100% Code coverage with those tests
7. Source Code contained within the jar
8. Javadoc contained within the jar
9. Type safety
10. Extremely limited use of reflection
11. Use of code analysis tools in their strictest sense

The creation of secure code is not easy, but you are biting the bullet
for all downstream users of your code, and allow them to build
their software on granite instead of sand.
