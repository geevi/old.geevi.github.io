---
layout: page
title: "Publications"
mathjax: enable
---
### Hardness of Coloring Problems

#### Hardness of Approximation

$P \equiv$ easy to solve (in polynomial time) problems.  
$NP \equiv$ problems for which solutions are easy to verify.


Solutions to sudoku puzzles, mathematical proofs etc. are easy to verify. But does that mean they are easy to come up with? Can creativity
be automated? 

*Hence the $P\neq NP$ Conjecture.*

**$3$-SAT**: Given clauses $C_1,\cdots,C_m$ where $C_i$ is of form $\neg x_1 \vee x_3 \vee \neg x_4 $, find an assignment that maximizes the no. of 
clauses satisfied.


*$P \neq NP$ implies not possible!*


*Can we get an assignment that satisfies $Cm$ clauses?*

Give a random assignment, $C=7/8$ fraction is
satisfied in expectation.

*Can we do better?*

##### Probabilistically Checkable Proofs (PCP)
 The proof for a \TSAT\ instance to be satisfiable is an assignment to the
 variables that satisfies all the clauses. To verify this proof, one might need to look at all the bits of the proof.
 PCP is a way of writing proofs, such that verification can be done by
 just looking at a few random bits.

**PCP Theorem:** There is a verifier and a way of encoding an assignment to a \TSAT\ instance into a probabilistically 
checkable proof, such that 

*  correct proofs corresponding to assignments which satisfy all clauses are accepted by the verifier,
*  wrong proofs are accepted with probability at most a constant $s$.
 
 
 
*PCP with $3$ random queries where verifier can apply $\neg$ to answers and check OR $\Leftrightarrow$  no algorithm with $C=s$.*

In 1998, Hastad constructed PCP with $s$ close to $7/8$. That is we cannot improve upon that stupid random algorithm.

*Without knowing this we would have wasted \$\$ trying to improve upon 7/8.*

Curious minds will ask: What is this magic number $7/8$ above which the problem is hard (requires
exponential time) and below which is easy (solvable in polynomial time) ? Are there similar no. for other
problems also? 

#### Graph Coloring
*Given a $3$-colorable graph, can you find a $C$-coloring?*

 Current best is $C = n^{0.199\cdots}$.  Known that finding a $4$-coloring  is NP-hard. 
 
*Where does the transition from easy to hard happen?*

##### Khot's Unique Games Conjecture (UGC)
Khot observed that *PCP with $2$ random queries and unique checks $\Rightarrow$ more  hardness of approximation results.*

 
##### Our Results

*In joint work with Irit Dinur, Prahladh Harsha, Srikanth Srinivasan~\cite{DHSV}, we showed that assuming a version of UGC, $C=2^{\poly(\log \log n)}$ is hard, an improvement over $C=\poly(\log \log n)$ hardness result of Dinur and Shinkar \cite{DinurS2010}.*

**Puzzle:** $N$ switches each of which can take $3$ positions, control a bulb which glows as red, blue and green. Changing the position of all the switches changes the color of the bulb. Show that the bulb is controlled
by exactly one switch.
   
Even if the number of colors the bulbs can take is $100$, for $N=1000$ this is still (al most) true~\cite{AlonDFS2004}.


*We show that even if the switches where not allowed to move independently, such statements are still true.*



#### Hypergraph Coloring

**$r$-Uniform Hypergraph:** A vertex set $V$ and a
collection of subsets of $V$ of size $r$. Assign colors to 
vertices such that no set is monochromatic.Graphs corresponds to the 
setting of $r=2$. 

*Known algorithms only guarantee $C=n^\alpha$ for some $\alpha < 1$. The state of the art results  showed that $C= \poly( \log n)$ is hard.*
 
##### Our Results
In joint work with Venkat Guruswami,
Johan H\aa stad, Prahladh Harsha and Srikanth Srinivasan~\cite{GHHSV}, we show $C>> \poly(\log n)$ is also hard.
Subsequent to our work, Khot and
Saket  showed $C=2^{(\log
n)^{1/19}}$ is hard~\cite{KhotS2014b}. Though their result was
for $12$-uniform hypergraphs. 
I further observed that
by combining their methods with ours, the same  hardness can be
obtained for $4$-uniform hypergraphs~\cite{Varma2014}. 

*Hence  we improved the hardness results from $C=\poly(\log n)$ to $C=2^{(\log n)^{1/19}}$ for the case of $4$-colorable $4$-uniform hypergraphs.*


#### Covering Problems
Covering problems are a generalization of the 
coloring problem. Motive for studying them is to develop
techniques which might later be adapted to graph coloring. 

An instance of the problem
consists of a hypergraph $G=(V,E)$ along with a *predicate* $P
\subseteq \{0,1\}^r$ and a *literal* function $L:E\rightarrow
\{0,1\}^r$. An *assignment* $f:V \rightarrow \{0,1\}$
*covers* an edge $e\in E$, if $f|_e \oplus L(e) \in P$. 
A *cover* for an instance is a set of 
assignments such that every edge is covered by one of the assignments.

**The covering problem is, given a $2$-coverable instance, find a $C$-covering?**

**Theorem:** $G$ has a cover of size $C$ with the not-all-equal predicate
$\{0,1\}^r \setminus \{ \overline 0, \overline 1\}$ iff it is
$2^C$-colorable. 

Some predicates like \TSAT\ which has an
\emph{oddness} property (for every $x\in \{0,1\}^r, x\in P \vee \bar x \in P$). Then $C=2$ is easy, since any assignment and its complement
covers the instance.
\para
Dinur and Kol asked the question
whether the covering problem is hard  for all non-odd
predicates for any constant $C$~\cite{DinurK2013}. Assuming a slightly modified form of UGC, they proceeded to show that if a non-odd predicate has a
pairwise independent distribution in its support, then this is indeed
the case.

##### Our Results
 In joint work with Amey Bhangale and Prahladh Harsha~\cite{BhangaleHV2014}, we show 
<ul>
<li> hardness for all non-odd predicates and for all constants $C$ (making same assumptions as Dinur and Kol),
<li> NP-hardness under some mild conditions on the predicate for $C= \log \log n$, 
<li> improved hardness of $C=\log \log n$ (Dinur and Kol proved $\log \log \log n$.).
</ul>



