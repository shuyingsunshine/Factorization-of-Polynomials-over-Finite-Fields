# Factorization-and-Decomposition-of-a-polynomial-over-finite-fields


Given a monic polynomial f over finite fields F, (i.e. the coefficents of f are in the field F), we will factor f into product of irreducible monic polynomials. (a polynomial is irreducible if it is not the product of two polynomials of positive degree.)

The algorithm is divided into 3 phases:

   1. square-free factorization : given monic polynomial f, find the square-free factorization of f (i.e. each factor appears only once)
   2. distinct degree factorization : given monic square-free polynomial, find the distinct degree factorization of f such that each factor is the product of all monic irreducible factors of f of the same degree
   3. equal degree factorization : given a monic square-free polynomial f of positive degree that is known to be the product of irreducible polynomials of degree d, find the factorization of f into irreducible factors. The algorithm we used is probabilistic algorithms. And we deal with the odd finite field and even finite field separately.
   

The implementation is based on magma.

In "gcd.txt", the code is for finding the greatest common divisor of two polynomials, which is similar to the idea of Eucleadian algorithm used in finding the greatest common divisor of two integers.

In "square_free_fact.txt", the code is for finding the sqaure-free factorization, which is pahse 1.

In "distinct_degree_fact.txt", the code is for splitting f into product of polynomials whose irreducible factors all have the same degree, which is phase 2.

In "equal_degree_factorization.txt", the code is for factor a square-free polynoimal which is the product of irreducible polynomials of the same degree, which is pahse 3.

In "factor.txt", the code is for factor any monic polynomial f over finite fields into products of irreducibles.


To use the factor function, first generate a finite field F, and then generate some polynomial f over F, then call factor(f).

Magma example code:

load "factor.txt";
p := 5;
e := 2;
F<g> := FiniteField(p,e);
P<x> := PolynomialRing(F);
n := 10;
f := random_poly(n,F);
factor(f);

   
