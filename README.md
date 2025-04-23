# libc
I would like to improve my fundamentals of low level programming so
i can contribute to production libcs such as llvm libc.

I would like to implement the math functions from `crlibm` and some c23 math functions.

some of the algorithms are simple but production systems such as llvm libm
have requirements such as performance and rounding to all modes so the
maintainers might use their own range reduction algorithms for performance
reasons.

for example, the handbook of floating point math functions introduce
`sin` with a range reduction algorithm that leads to 4 branches which in a production
system if you care about performance/throughput is not acceptable.

and most double precision math functions are implemented with double double
arithmetic.

and you also need to worry about ulp and so on.

so obviously production systems have more requirements. but ive seen some
other production libraries and its not too shabby.

i just need to learn the fundamentals
and the
llvm libc/libm interface so ill mimic the llvm libc interface so i will try
to implement functions such as getting the exponent, mantissa and so on so i can understand this.

anyways the above comments and `fmul.cpp` are based on what ive learned in my
open source llvm libc experience.

and also i want to write my own unix kernel and according to the os wiki
i need to write my own subset of libc. so mind as well get started with this.
ill probably just see what the xv6 unix kernel and just port it c++ using
oo programming. then i rewrite my own one in C or even in common lisp hehe.

llvm libc has been a very challenging project that ive been involved in but
i need to get the basics down by writing my own thing before i can be more
productive in llvm libc.
