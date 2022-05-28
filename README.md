# QuaternionIsomorphisms
Magma implementation of our algorithm for computing an explicit isomorphism between quaternion algebras over a quadratic function field in odd characteristic.

## Usage
In order to try this code, simply type ```load "init.magma";```
Then, you may try to use the functions from the file test_functions.magma to execute the various subroutines of the algorithm.

## Benchmarks
Some specific tests are available in the benchmarks repertory. To us one, simply load the corresponding file in Magma from the root directory of the repository. There is no need to load init.magma first. Since the output can be verbose, you will be prompted for the path to an output file. Leave the prompt empty to print results directly in the standard output instead.

## Bibliograpy
Some references to the literature are given in the source code. Here is the list of references used. This is a subset of the bibliography of our article, which should be consulted for more details on the theoretical foundations of this implementation.


//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
//								Bibliography:												//
//	[1] A. K. Lenstra - Factoring Multivariate Polynomials over Finite Fields, 1984											//
//	[2] G. Ivanyos, P. Kutas, L. Rónyai - Computing Explicit Isomorphisms with Full Matrix Algebras over Fq(x), 2018						//
//	[3] L.Rónyai - 	Computing the Structure of Finite Algebras, 1990												//
//	[4] W.A de Graaf, G. Ivanyos, A. Küronya, L.Rónyai - Computing Levi Decompositions in Lie algebras, 1997							//
//	[5] G.Ivanyos, P.Kutas, L.Rónyai - Explicit equivalence of quadratic forms over Fq(t), 2018									//
//	[6] J.Gómez-Torrecillas, P.Kutas, F.J.Lobillo, G.Navarro - Primitive idempotents in central simple algebras over Fq(T) with applications to coding theory	//
//////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////
