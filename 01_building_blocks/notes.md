## Covered rules
#### Writing a `main()` method
1. Each file can contain only one `public` class
2. The filename must match the calss name including case and have a `.java` extension.
3. if the java class is an entry point for the program, it must contain a valid `main()` method.
#### Creating objects
4. Fields and instance initializer blocks are run in the order in which they appear in the file. 
5. The constructor runs after all fields an instance initializer blocks have run. 
#### Understanding data types
6. The `byte`, `short`, `int` and `long` types are used for integer values without decimal points.
7. Each numeric type uses twice as many bits as the smaler simialr type. for example, `short` uses twice as mnay bits as `byte` does.
8. All of the numeric types are signed and reserve one of their bits to cover a negative range. For example, instead of `byte` covering 0 to 255, it actually covers -128 to 127
9. A float requires the letter `f` or `F` foloowing the number so java knows it is a float. Without an `f` or `F`, java interprets a decimal value as a `double`.
10. A `long` requires the letter `l` or `L` following the number so java knows it is a `long`. Wihtou an `l` or `L`, java interprets a number without a decimal point as an int in most scenarios. 

## Command tips
- run `javac -d classes <file-paths>` to compile all the files to the `classses` directory.
- run compiled classes from `classes` directory by running `java -cp classes <file-path>`