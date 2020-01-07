# How to compile and run a program

## Compiling
If you are trying to compile a C program you can use `gcc` or `icc` and if you
  are trying to compile a Fortran program you can use `gfortran` or `ifort`.

Compile the program

```
$ gcc helloworld.c
```
This will produce the executable `a.out` which you can run by entering

```
$ ./a.out
hello world!
```

You can choose the name of executable produced by using the `-o` flag

```
$ gcc helloworld.c -o hello
```
and now this will work.
```
$ ./hello
hello world!
```


To see the command line arguments for a compiler type
```
$ gcc --help
```
or
```
$ man gcc
```
The `man` stands for manual and is often available for every executable installed.