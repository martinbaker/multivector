Multivector
-----------
Code to use with FriCAS program - I shold really change the name from 'Multivector' becaulse its no longer just about Clifford algebra but is a place to publish my new FriCAS code on any subject.

Changes Jan 2016
----------------
I have made some changes and additions to some of my code. Would you be interested in including this in the FriCAS library?

The changed/new files are:

<ul>
  <li>logic.spad</li>
  <li>graph.spad</li>
  <li>algebraictopology.spad</li>
  <li>computation.spad</li>
</ul>
These files are available here:
https://github.com/martinbaker/multivector

These 4 files are interdependent so it would be really good, from my point of view, if you could include all of them.

Further details of the changes are:

logic.spad
----------
This is new code. Includes various logic related structures including partial order, lattice structures

I have also moved intuitionistic logic here from computation.spad

Since I last mentioned this on the forum I was kindly sent some unpublished code (related to Moebius function) by Franz Lehner with permission to merge this with my own poset related code. This is now all included in the code on Github.

These are my notes related to the code written by Franz:
http://www.euclideanspace.com/prog/scratchpad/mycode/discrete/logic/moebius/

I have included Logic category, this is the same as existing Logic
category in Boolean.spad as it is intended to replace it. Since this
category is more general than just Boolean I thought it more appropriate
to put it in logic.spad. 

For further information see the documentation here:<ul>
  <li>http://www.euclideanspace.com/prog/scratchpad/mycode/discrete/logic/</li>
  <li>http://www.euclideanspace.com/prog/scratchpad/mycode/discrete/logic/moebius/</li>
</ul>
graph.spad
----------
There are some updates to existing code, this includes:

1) Fix bug in spanningTree since old version sometimes put a given node at multiple leaves in the tree.

2) Add coercions and constructors from FinitePoset.

3) Improve documentation.

4) Improve output code.

For further information see the documentation here:

http://www.euclideanspace.com/prog/scratchpad/mycode/discrete/graph/

algebraictopology.spad
----------------------
This is new code.

This includes simplicial complexes. At the moment only abstract simplicial complexes (purely combinitorial) are operational. The plan is to add geometric complexes later.

My aim is also to export to homotopy and homotopy groups.

For further information see the documentation here:
http://www.euclideanspace.com/prog/scratchpad/mycode/topology/simplex/

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

3) Homology - Can we use simplicial complex to generate the Smith normal form which already exists in FriCAS?

4) Homotopy - Although a lot of stuff in homotopy does not have a general algorithmic solution, I would still like to be able to generate groups from complexes. This would require implementing groups as presentations (free groups). I realise there are limitations on what can be done with these but, as an example GAP can do some simplifications of such groups. Franz tells me he has implemented code for free products of groups so it would be interesting to see if this could be merged in.


