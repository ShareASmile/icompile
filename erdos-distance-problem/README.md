<a href="http://en.wikipedia.org/wiki/Combinatorial_geometry">Combinatorial  incidence geometry</a> is the study of the possible combinatorial  configurations between geometric objects such as lines and circles. One  of the basic open problems in the subject has been the <a href="http://www.cs.umd.edu/%7Egasarch/erdos_dist/erdos_dist.html">Erd?s  distance problem</a>, posed in 1946:
<blockquote><strong>Problem 1 (Erd?s distance problem)</strong> Let <img title="{N}" src="http://l.wordpress.com/latex.php?latex=%7BN%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{N}" /> be a large natural number. What is  the least number <img title="{\\# \\{  |x_i-x_j|: 1 \\leq i &lt; j \\leq N \\}}" src="http://l.wordpress.com/latex.php?latex=%7B%5C%23+%5C%7B+%7Cx_i-x_j%7C%3A+1+%5Cleq+i+%3C+j+%5Cleq+N+%5C%7D%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{\\# \\{ |x_i-x_j|: 1 \\leq i &lt; j \\leq N \\}}" /> of distances that  are determined by <img title="{N}" src="http://l.wordpress.com/latex.php?latex=%7BN%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{N}" /> points <img title="{x_1,\\ldots,x_N}" src="http://l.wordpress.com/latex.php?latex=%7Bx_1%2C%5Cldots%2Cx_N%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{x_1,\\ldots,x_N}" /> in the  plane?</blockquote>
Erd?s called this least number <img title="{g(N)}" src="http://l.wordpress.com/latex.php?latex=%7Bg%28N%29%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{g(N)}" />. For instance, one can check  that <img title="{g(3)=1}" src="http://l.wordpress.com/latex.php?latex=%7Bg%283%29%3D1%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{g(3)=1}" /> and <img title="{g(4)=2}" src="http://l.wordpress.com/latex.php?latex=%7Bg%284%29%3D2%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{g(4)=2}" />, although the precise  computation of <img title="{g}" src="http://l.wordpress.com/latex.php?latex=%7Bg%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{g}" /> rapidly becomes more difficult  after this. By considing <img title="{N}" src="http://l.wordpress.com/latex.php?latex=%7BN%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{N}" /> points in arithmetic progression,  we see that <img title="{g(N) \\leq N-1}" src="http://l.wordpress.com/latex.php?latex=%7Bg%28N%29+%5Cleq+N-1%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{g(N) \\leq N-1}" />. By  considering the slightly more sophisticated example of a <img title="{\\sqrt{N} \\times \\sqrt{N}}" src="http://l.wordpress.com/latex.php?latex=%7B%5Csqrt%7BN%7D+%5Ctimes+%5Csqrt%7BN%7D%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{\\sqrt{N} \\times \\sqrt{N}}" /> lattice grid (assuming that <img title="{N}" src="http://l.wordpress.com/latex.php?latex=%7BN%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{N}" /> is a square number for  simplicity), and using some analytic number theory, one can obtain the  slightly better asymptotic bound <img title="{g(N) = O( N / \\sqrt{\\log  N} )}" src="http://l.wordpress.com/latex.php?latex=%7Bg%28N%29+%3D+O%28+N+%2F+%5Csqrt%7B%5Clog+N%7D+%29%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{g(N) = O( N / \\sqrt{\\log N} )}" />.

<!--more-->

On the other hand, lower bounds are more difficult to obtain. As  observed by Erd?s, an easy argument, ultimately based on the incidence  geometry fact that any two circles intersect in at most two points,  gives the lower bound <img title="{g(N) \\gg N^{1/2}}" src="http://l.wordpress.com/latex.php?latex=%7Bg%28N%29+%5Cgg+N%5E%7B1%2F2%7D%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{g(N) \\gg N^{1/2}}" />. The  exponent <img title="{1/2}" src="http://l.wordpress.com/latex.php?latex=%7B1%2F2%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{1/2}" /> has been slowly increasing  over the years by a series of increasingly intricate arguments combining  incidence geometry facts with other known results in combinatorial  incidence geometry (most notably the <a href="http://en.wikipedia.org/wiki/Szemer%C3%A9di%E2%80%93Trotter_theorem">Szemer?di-Trotter  theorem</a>) and also some tools from additive combinatorics; however,  these methods seemed to fall quite short of getting to the optimal  exponent of <img title="{1}" src="http://l.wordpress.com/latex.php?latex=%7B1%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{1}" />. (Indeed, previously to last week,  the best lower bound known was approximately <img title="{N^{0.8641}}" src="http://l.wordpress.com/latex.php?latex=%7BN%5E%7B0.8641%7D%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{N^{0.8641}}" />, due to <a href="http://www.ams.org/mathscinet-getitem?mr=2065258">Katz and Tardos</a>.)

Very recently, though, <a href="http://arxiv.org/abs/1011.4105">Guth and  Katz</a> have obtained a near-optimal result:
<blockquote><strong>Theorem 2</strong> <a name="gk0"></a> One has <img title="{g(N) \\gg N / \\log N}" src="http://l.wordpress.com/latex.php?latex=%7Bg%28N%29+%5Cgg+N+%2F+%5Clog+N%7D&amp;bg=ffffff&amp;fg=000000&amp;s=0" alt="{g(N) \\gg N / \\log N}" />.</blockquote>
The proof neatly combines together several powerful and modern tools in a  new way: a recent geometric reformulation of the problem <a href="http://arxiv.org/abs/1005.0982">due to Elekes and Sharir</a>; the  polynomial method as used recently by Dvir, Guth, and Guth-Katz on  related incidence geometry problems (and <a href="http://terrytao.wordpress.com/2008/03/24/dvirs-proof-of-the-finite-field-kakeya-conjecture/">discussed  previously on this blog</a>); and the somewhat older method of cell  decomposition (also <a href="http://terrytao.wordpress.com/2009/06/12/the-szemeredi-trotter-theorem-and-the-cell-decomposition/">discussed  on this blog</a>). A key new insight is that the polynomial method (and  more specifically, the <em>polynomial Ham Sandwich theorem</em>, <a href="http://terrytao.wordpress.com/2008/11/27/the-kakeya-conjecture-and-the-ham-sandwich-theorem/">also  discussed previously on this blog</a>) can be used to efficiently  create cells.

In this post, I thought I would sketch some of the key ideas used in the  proof, though I will not give the full argument here (the paper itself  is largely self-contained, well motivated, and of only moderate length).  In particular I will not go through all the various cases of  configuration types that one has to deal with in the full argument, but  only some illustrative special cases.

To simplify the exposition, I will repeatedly rely on 