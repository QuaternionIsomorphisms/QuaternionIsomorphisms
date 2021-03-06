# QuaternionIsomorphisms
Magma implementation of our algorithm for computing an explicit isomorphism between quaternion algebras over a quadratic function field in odd characteristic.

## Prepared examples
Tailored self contained example files executing key subroutines of the algorithm can be found in the examples/ directory. Simply load magma (make sure to load it from the root directory of the repository) and type ```load "examples/*nameofexamplefile*.magma";```  
The subroutines tested here are the ones which are too slow for terminating with the input size needed for the algorithm. Hence we use smaller inputs here to showcase correctness of the algorithms and their implementation.  
The timings given here were obtained using an Intel i7-7700 CPU with four cores at 3.60 GHz.  
The tailored example files are the following:

### RationalSplit.magma
This file showcases the computation of an explicit isomorphism from a randomly generated algebra A to M_3(F_5(x)).  
On our machine, the test normally terminates in under 15 minutes.

### QuaternionSubalgebra.magma
This file generates a random quadratic extension Kext of the field K = F_3(x). It then generates a random algebra A isomorphic to M_2(Kext) and computes a subalgebra AK of A that is a quaternion algebra over K.
The technique used here is the novel idea from our work. In the context of our algorithm for computing explicit isomorphisms between quaternion algebra over Kext, it is untractable because it would involve computing a rank one idempotent in a 256 dimensional K-algebra. Here, we showcase the technique on the more modest input of a quaternion Kext-algebra, and therefore it is only needed to compute an idempotent in a 16 dimensional K-algebra.  
The timing for execution here may vary a lot. We recommend aborting and restarting if it takes longer than 20 minutes (based on our observation, relative to the CPU we used).

## Usage
It is also possible to interact with the code directly. Again, launch magma from the root directory of the repository and type ```load "init.magma";```
Then, you may want to use the functions from the file test_functions.magma to see the execution of the various subroutines of the algorithm.
Please note that until more efficient computation of maximal order is available, the whole algorithm will not terminate in a reasonable time.

## Bibliography
Some references to the literature are given in the source code. Here is the list of references used. This is a subset of the bibliography of our article, which should be consulted for more details on the theoretical foundations of this implementation.


1. A. K. Lenstra - Factoring Multivariate Polynomials over Finite Fields, 1984
2. G. Ivanyos, P. Kutas, L. R??nyai - Computing Explicit Isomorphisms with Full Matrix Algebras over Fq(x), 2018
3. L.R??nyai - 	Computing the Structure of Finite Algebras, 1990
4. W.A de Graaf, G. Ivanyos, A. K??ronya, L.R??nyai - Computing Levi Decompositions in Lie algebras, 1997
5. G.Ivanyos, P.Kutas, L.R??nyai - Explicit equivalence of quadratic forms over Fq(t), 2018
6. J.G??mez-Torrecillas, P.Kutas, F.J.Lobillo, G.Navarro - Primitive idempotents in central simple algebras over Fq(T) with applications to coding theory
