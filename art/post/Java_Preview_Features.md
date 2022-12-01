![tag](https://img.shields.io/badge/article-Instagram-red.svg)
# Java Preview Features
![](./Key_Dates_In_Java_History/01.png)
<div component="text-block">
Even before first public release in March 1995, Java community continuously collecting feedbacks to deliver that software
developers have told them they need. One of the processes to achieve that is a Preview Feature, specified in JEP 12.

A preview feature is a new feature whose design, specification, and implementation are complete, but which is not permanent, 
which means that the feature may exist in a different form or not at all in future JDK releases.
</div>

# Java Preview Features
![](./Key_Dates_In_Java_History/01.png)
<div component="text-block">

With Java 17 release become available _"JEP 406: Pattern Matching for switch (Preview)"_, with that we can write something
like this:

```java
public class PreviewFeature {
    public static void main(String[] args) {
        System.out.println(formatterPatternSwitch(11L));
    }

    static String formatterPatternSwitch(Object o) {
        return switch (o) {
            case Integer i -> String.format("int %d", i);
            case Long l    -> String.format("long %d", l);
            case Double d  -> String.format("double %f", d);
            case String s  -> String.format("String %s", s);
            default        -> o.toString();
        };
    }
}
```
This code could be used as a validator of enabling/disabling preview feature. Alongside with examples, it could be found at: //todo: insert git link.
</div>

