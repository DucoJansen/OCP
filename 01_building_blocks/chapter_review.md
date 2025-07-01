# Chapter 1 review

1. D,E
2. C,D,E
3. A,E
4. B,E,G (maybe D as well? But I say no now.)
5. A,D,F
6. G (it's 8)
7. F (`numKnives` is not initialized)
8. B, G, H
9. E (A and B default to wrong thing i think, local instances don't default at all i think.)
10. A, E, F
11. E, 4 (i think java.lang is always )
12. A (syntax is wrong)
13. A, B, C (a uses aquarium, b uses aquarium, c uses jellies, d doesn't know, e is inconclusive)
14. A, B, D, E (`long` can't be boxed to `short`, `double` can't be stored in `int`, `short` doesn't have `.length()`
    method, `int` doesn't have attribute `length`)
15. C, F (i purposely did not choose the options with "never" or "always")
16. A, E (I forgot the rules about this)
17. D, F, G (check how `private`/`public` variables instantiate) (and check why line 7 doesn't generate compile error)
18. B, D, F, G
19. A, E (check difference between `parseXXX()` and `valueOf()`)
20. E
21. F (I think the codeblocks are executed before the initialization of `count`)
22. G (all the others either have wrong type assignments, or number is too big, or `_` are wrong)
23. A (`double` can't be assigned to `float`(?))

### Questions that arose during the review (to check later)

- Q: Under what circumstances can i not use `var`.
- Q: To what values to certain types default? To what values do primitives default?
- Q: When do multiline print lines leave trailing whitespaces or when do they go on a new line?
- Q: Do codeblocks get executed before other stuff? E.g. in what order does this execute

```java
public class River {
    int count;

    {
        System.out.println(count + '-');
    }

    {
        count++;
    }
}
```

# Results

1. <span style="color:green;">Correct</span>
2. <span style="color:green;">Correct</span>
3. <span style="color:green;">Correct</span>
4. <span style="color:green;">Correct</span> (D was not correct because a `.` is not allowed in an identifier. It also
   makes sens because otherwise what
   would happen if the identifier contains a reference to a method? identifier `a.b` with method `c()` would look
   like `a.b.c()` which obviously would cause confusion (besides the fact that it doesn't compile)).
5. <span style="color:green;">Correct</span>.
6. <span style="color:red;">Wrong</span>. It was F (7), variables within `{}` are only in scope within the `{}`
7. <span style="color:red;">Wrong</span>, C, E. `numKnives` is indeed not initialized, but also not accesses. Because *
   *everything** within the print is
   a comment because of `"""..."""`
8. <span style="color:orange;">Wrong</span> B, **D**, **E**, H (not G). (A: `var` can't be initialized with `null` (can
   be
   later assigned with `null` if
   type is not primitive),E: dividing by 0 results in Runtime Exception, not compile error, G: `var` can't be used in
   multiple variable assignment)
9. <span style="color:green;">Correct</span>. local variables indeed don't have default values (C and D thus
   incorrect). `float` default should have decimal point.
10. <span style="color:green;">Correct</span>.
11. <span style="color:green;">Correct</span>. Indeed `java.lang` is always imported.
12. <span style="color:yellow;">Wrong</span>, A, **C and D**. C bc java does not support default param values, and D
    bc `fins` is only in scope in the `{}`.
13. <span style="color:green;">Correct</span>. Exactly correct
14. <span style="color:green;">Correct</span>.
15. <span style="color:yellow;">Wrong</span>. C, **E**, F. E is true because a program can end _before_ garbage
    collection runs.
16. <span style="color:orange;">Wrong</span>. A, **D** (not E) .`\` means to skip the linebreak.
17. <span style="color:green;">Correct</span>. Class variables in general instantiate to default values.
18. <span style="color:orange;">Wrong</span>. B, **C**, F (not D and G). `var` can't be used for class variables. `var`
    can't be used in multiple assignments. `var` is not reserved in java
19. <span style="color:orange;">Wrong</span>. A, **D** (not E). `parseLong` returns primitive `long` and `valueOf`
    returns wrapper class `Long`.
20. <span style="color:red;">Wrong</span>. **C**. Key thing to note is that the `PoliceBox()` is not a constructor but a
    method (that is never called).
21. <span style="color:red;">Wrong</span>. My comment was true, but `count` had a default initialization of `0` since it
    was a class variable, so it compiles fine .
22. <span style="color:yellow;">Wrong</span>. **C, F**, G. C and F. `0x` is start of hexadecimal and `0b` is start of
    binary number so that's all fine.
23. <span style="color:yellow;">Wrong</span>. A, **D**. `depth` was only in scope in `for`.

### result 11/23 correct