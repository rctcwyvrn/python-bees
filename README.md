python-bees
---

An implementation of the Artifical Bee Colony algorithm originally proposed by Karaboga

ABC_test.py attempts to reverse a step of a cellular automata using the ABC algorithm. 

The algorithm currently can find around 100 solutions very quickly, but can't find many more.
I believe the current main problem is not with the bees, but rather because hamming distance is not great for determing how good a solution is, and also the improvement strategy of flipping one bit at a time can only get so many solutions.

Another big problem is that this application is not what this sort of meta-heuristic is usually used for. Reversing cellular automata requires finding all 10k ish possible steps, while the ABC algorithm is very good at finding one solution out of a large amount.

Results
---

*Good runs*

TOTAL TIME FOR 100 SOLUTIONS =  4.619204521179199 FOR RANDOM_GOAL= True
AVERAGE TIME FOR 10 CYCLES= 3.7850918769836426
CYCLE COUNT= 15
STD DEV in solution times= 0.21309670614425877

TOTAL TIME FOR 100 SOLUTIONS =  5.018507242202759 FOR RANDOM_GOAL= True
AVERAGE TIME FOR 10 CYCLES= 4.860507488250732
CYCLE COUNT= 11
STD DEV in solution times= 0.27361129124608474

*Bad runs*
They never finish because they get stuck at solutions with a hamming distance of 2, and flipping bits isn't enough to fix it.