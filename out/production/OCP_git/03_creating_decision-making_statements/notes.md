# Notes chapter 3
#### Selecting switch data types
The target of a switch statement is allowed to be of the following types:
- int and Integer
- byte and Byte
- short and short
- char and Character
- String 
- enum values
- var (if the type resolves to one of the above at runtime)

notice that boolean, long, float and double are excluded (as are Boolean, Long, Float and Double). The reasons vary, such as boolean having too small range of values, and floating-point numbers having quite a wide range of values. 

