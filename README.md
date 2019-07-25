python-bees
---

An implementation of the Artifical Bee Colony algorithm originally proposed by Karaboga

ABC_test.py attempts to reverse a step of a cellular automata using the ABC algorithm. 

The algorithm currently can find around 100 solutions very quickly, but can't find many more.
I believe the current main problem is not with the bees, but rather because hamming distance is not great for determing how good a solution is, and also the improvement strategy of flipping one bit at a time can only get so many solutions.