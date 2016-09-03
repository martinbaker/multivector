Multivector
-----------
Code to use with FriCAS program - I should really change the name from 'Multivector' because its no longer just about Clifford algebra but is a place to publish my new FriCAS code on any subject.

Since release 1.3.0 the algebraic topology code is now included in the FriCAS library. However there are some outstanding issues to be sorted out and ongoing maintenance so I have moved algebraic topology and logic code to a new repository here: https://github.com/martinbaker/fricasAlgTop .

The plan is to also move other topics out to their own repositories.

graph.spad
----------
There are some updates to existing code, this includes:

1) Fix bug in spanningTree since old version sometimes put a given node at multiple leaves in the tree.

2) Add coercions and constructors from FinitePoset.

3) Improve documentation.

4) Improve output code.

For further information see the documentation here:

http://www.euclideanspace.com/prog/scratchpad/mycode/discrete/graph/


computation.spad
----------------
There are some updates to existing code, this includes:

5) Remove intuitionistic as I have now put it in logic.spad

6) Improve documentation.

7) Improve output code.

For further information see the documentation here:
http://www.euclideanspace.com/prog/scratchpad/mycode/computation/

TODO
----
There is a lot more work to be done on this code but I think it is in a state where it can be of some use to others. If it is included in the FriCAS library then there is always a chance that someone else may be able to help. I would welcome as much help as I can get.

Some improvements I would like to make at some time in the future are:

1) I would like to fully implement the geometric version of simplicial complex. One reason is that I would like to make it the standard way to represent 2D, 3D and n-dimensional shapes in code such as scene.spad. So the shapes can be transformed and output in various ways however they would have better mathematical properties than the structures usually used to represent shapes in computer science. This would involve writing code to test for overlapping simplexes and so on.

2) The code that Franz Lehner sent to me also included isomorphism testing and drawing (using algorithms from Freese's book on "Free Lattices"). I would like to merge this with my code. (it may not all be generalisable to graphs/complexes but parts of it may be and the remainder can still be used for posets).



