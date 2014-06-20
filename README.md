﻿## Comparison of Programming Languages in Economics

This project contains the source code referenced in the paper [A Comparison of
Programming Languages in Economics][1] by S. Borağan Aruoba and Jesús
Fernández-Villaverde.

The main fork will remain basically unchanged to allow researchers to check our
basic results.

### Abstract from the paper

> We solve the stochastic neoclassical growth model, the workhorse of modern
> macroeconomics, using `C++11`, `Fortran 2008`, `Java`, `Julia`, `Python`,
> `Matlab`, `Mathematica`, and `R`. We implement the same algorithm, value
> function iteration with grid search, in each of the languages. We report the
> execution times of the codes in a `Mac` and in a `Windows` computer and
> comment on the strength and weakness of each language.

## Files

1. `RBC_CPP.cpp`: C++ code. 
2. `RBC_F90.f90`: Fortran code.
3. `RBC_Java.java`: Java code.
4. `RBC_Julia.jl`: Julia code, to run RBC_Julia; @time main().
5. `RBC_Matlab.m`: Matlab code.
6. `RBC_Matlab_Inside_Loop.m`: Matlab code with Mex file.
7. `inside_loop_mex.cpp`: Mex file for 5.
8. `RBC_Python.py`: Python code for CPython and Pypy.
9. `RBC_Python_Numba.py`: Python code for Numba.
10. `RBC_R.R`: R code.
11. `RBC_R_Compiler.R`: R code compiled.
12. `RBC_Mathematica`: Mathematica code.
13. `RBC_Mathematica_Imperative`: Mathematica code with imperative structure.
14. `RBC_Mathematica_PartialCompilation`: Mathematica code with imperative
    structure and partial compilation.
15. `RBC_Mathematica_Plain_Text.tx`: Mathematica code in plain text for those
    without Mathematica.
16. `RBC_Mathematica_Imperative_Plain_Text.text`: Mathematica code in plain
    text, imperative version.

## Compilation flags

1. GCC compiler (Mac): `g++ -o testc -O3 RBC_CPP.cpp`
2. GCC compiler (Windows): `g++ -Wl,--stack,4000000, -o testc -O3 RBC_CPP.cpp`
3. Clang compiler: `clang++ -o testclang -O3 RBC_CPP.cpp`
4. Intel compiler: `icpc -o testc -O3 RBC_CPP.cpp`
5. Visual C: `cl /F 4000000 /o testvcpp /O2 RBC_CPP.cpp`
6. GCC compiler: `gfortran -o testf -O3 RBC_F90.f90`
7. Intel compiler: `ifortran -o testf -O3 RBC_F90.f90`
8. `javac RBC_Java.java` and run as `java RBC_Java -XX:+AggressiveOpts`

In all cases with a JIT, you may want to warm up the JIT before testing for
speed.

[1]: http://economics.sas.upenn.edu/~jesusfv/comparison_languages.pdf
