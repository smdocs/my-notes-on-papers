# Steps to prove a problem X is NP Complete

> General Idea: In order to prove that a problem is NP complete,we need to show that ot is noth in NP and at least as <b>hard</b> as any other 
problem in NP.

### [Step 1: Show that problem X is in NP]()
Argue that there is an efficient verifier for X. In other words, describe a verifier such that for any yes instance of X, there exists a certificate that the verifier will accept, and for any no instance of X, no such certificate exists. The running
time of the verifier (and hence the size of the certificate) must be polynomial. Typically, a solution to the given problem is a sufficient certificate. This step is very brief, but necessary.

### [Step 2: Pick a know NP complte problem]()
State what problem Y we are reducing to X; we need to show that Y ≤P X.  By the very definition of NPcomplete, if X is NP-complete, then we can technically use any other NP-complete problem Y to show this. However, some problems will be far easier to use than others.It is often useful to spend some time thinking about which of the problems we know to be NP-complete would be most natural to use for a given reduction.

### [Step 3: Construct an algorithm to solve Y given an algorithm to solve X]()
Show that a instance of Y can be solved using a polynomial number of operations, and a polynomial number of calls to a black box that can solve X. Note: It is very easy to get mixed up and instead prove that X ≤p Y . Unfortunately, this is not what we want to show (we already know that Y is NP-complete).

Typically, we will show how to solve Y by constructing a single input to the black box for X, and typically, our algorithm will output the same answer as is given by the black box. However, this is not always the case (in which case, define the correspondence between the output of the black box for X and the desired solution for Y.)

### [Step 4: Prove the correctness of the algorithm to solve Y]()
This requires proving an if and only if statement. It is always trivial to come up with an algorithm that satisfies just one of these two conditions. We want something that satisfies both.

Step 4a: Prove the solution is correct. Show that if our algorithm returns “yes,” then the given input is indeed a yes instance of Y .
Step 4b: Prove that we find all solutions . Show that if we are given a yes instance of Y , then our algorithm returns “yes”.

### [Step 5: Deduce running time and wrap up.]()
Make sure that your construction to be used with the black box for X is poly-size and poly-time. This should allow us to conclude that since our algorithm runs in polynomial time, Y ≤P X. Since Y is NP-complete, and since we also have shown that X is in NP, X is NP-complete
