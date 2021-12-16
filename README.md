# Optimization
Level 1 and 2 are implemented in python language. In python I used Pulp for Linear Programming.
Pulp can only do linear models so for higher levels I couldn’t use it.
I tried to use Pyomo for nonlinear problems but couldn’t get the results I wanted and couldn’t find any better library with a good documentation so I decided to change the language to Julia for better results.
At first I used JuMP, it was easy to use but not efficient and optimal (over 10 GB of memory for E.Coli using Second-order cone constraint😐) but it could solve level 3 problem.
Next, I found Convex.jl that is better and easier for implementing Second-order Cone and Quadratic problems. I used this library to solve other levels, and even got better result for level 3.
For solving problems, I used the hints in the questions and almost got acceptable results.
I solved last problem as it was formulated in the question and for 0-norm I used this function:
min⁡ ∑▒f(x_i ) 
s.t.       Ax=y
Were f(x) is:
f(x_i )=exp⁡(-(x_i^2)/(2δ^2 ))
And δ is a positive number approaching 0.
 
