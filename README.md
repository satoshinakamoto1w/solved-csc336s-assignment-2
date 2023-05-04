Download Link: https://assignmentchef.com/product/solved-csc336s-assignment-2
<br>
Please write your family and given names and <strong>underline </strong>your family name on the front page of your paper.

All questions <strong>must </strong>be written in latex, and compiled to a single pdf. Plots (3 for Q2 and 1 for Q3) must in embedded in latex. All code and output of Q2 and Q3 should be <em>embedded </em>into latex. Code and output should be embedded with fixedwidth fonts, e.g. Courier. Font size of all fonts must be 12. Linespacing set to 1.1.

What to submit:

<ul>

 <li>The single pdf file 00A2.pdf (with embedded code and output).</li>

 <li>The latex source file of A2.</li>

 <li>Any source code you wrote (for computation, plots, etc).</li>

 <li>Plot files (7 for Q2 and 1 for Q3) in eps and png format.</li>

</ul>

(If subplot is used for the last 4 plots of Q2, then this gives only one file, so a total of 4 files for Q2.) Thus, the code and plots will be available within latex/pdf, <em>as well as </em>separately.

<ol>

 <li>Consider the matrix <em>A </em>and its inverse <em>A</em><sup>−1</sup>,</li>

</ol>

   6        13    −17               6      − 4     − 1 

<em>A </em>= <sup> </sup>13       29    −38   <em>A</em>−1 = <sup> </sup>− 4      11        7 <sup></sup>.

                                                         

−17   −38      50             − 1       7         5 

<ul>

 <li>[<em>3 points</em>] What is the condition number of <em>A </em>in the infinity norm?</li>

 <li>[<em>6 points</em>] Suppose we solve <em>Ax </em>= <em>b </em>for some <em>b</em>, and obtain <em>x</em>ˆ, so that ||<em>b </em>− <em>Ax</em>ˆ||<sub>∞ </sub>≤ 01. How small an upper bound can be found for the absolute error ||<em>x </em>− <em>x</em>ˆ||<sub>∞</sub>? Giv e the bound as a numerical value.</li>

</ul>

|| ˆ<em>x </em>− <em>x</em>||<sup>∞</sup>

<ul>

 <li>[<em>6 points</em>] With the same situation as in (b), how small an upper bound can be found for the relative error ?</li>

</ul>

||<em>x</em>||<sub>∞ </sub>Give the bound in terms of ||<em>b</em>||<sub>∞</sub>.

<ol start="2">

 <li>A group of <em>n </em>parachutists each with given mass <em>m<sub>i </sub></em>and drag coefficient <em>c<sub>i</sub></em>, <em>i </em>= 1,…, <em>n</em>, are connected by a weightless cord, and are falling at a given velocity <em>v</em>. We would like to calculate the tension <em>t<sub>i</sub></em>, <em>i </em>= 1,…, <em>n </em>− 1, in each section of the cord and the acceleration <em>a </em>of the whole group. Let’s index the parachutists from top (<em>i </em>= 1) to bottom (<em>i </em>= <em>n</em>), and let <em>g </em>= 9. 81 be the acceleration of gravity. For the top parachutist (<em>i </em>= 1), Newton’s second law giv es the equation</li>

</ol>

<em>t</em><sub>1 </sub>+ <em>m</em><sub>1</sub><em>g </em>− <em>c</em><sub>1</sub><em>v </em>= <em>m</em><sub>1</sub><em>a</em>

which can be written as

<em>t</em><sub>1 </sub>− <em>m</em><sub>1</sub><em>a </em>= <em>c</em><sub>1</sub><em>v </em>− <em>m</em><sub>1</sub><em>g</em>.                                             (1)

For an arbitrary ‘‘interior’’ parachutist indexed <em>i</em>, <em>i </em>= 2, . . . , <em>n </em>− 1, Newton’s second law giv es the equation

−<em>t<sub>i</sub></em>−<sub>1 </sub>+ <em>t<sub>i </sub></em>+ <em>m<sub>i</sub>g </em>− <em>c<sub>i</sub>v </em>= <em>m<sub>i</sub>a</em>

which can be written as

−<em>t<sub>i</sub></em>−<sub>1 </sub>+ <em>t<sub>i </sub></em>− <em>m<sub>i</sub>a </em>= <em>c<sub>i</sub>v </em>− <em>m<sub>i</sub>g                                        </em>(2)

For the bottom parachutist (<em>i </em>= <em>n</em>), Newton’s second law giv es the equation

−<em>t<sub>n</sub></em>−<sub>1 </sub>+ <em>m<sub>n</sub>g </em>− <em>c<sub>n</sub>v </em>= <em>m<sub>n</sub>a</em>

which can be written as

−<em>t<sub>n</sub></em>−<sub>1 </sub>− <em>m<sub>n</sub>a </em>= <em>c<sub>n</sub>v </em>− <em>m<sub>n</sub>g                                           </em>(3)

For convenience, let’s denote the unknown <em>a </em>by <em>t<sub>n</sub></em>. Writing equations (1), (2) for <em>i </em>= 2,…, <em>n </em>− 1 and (3) <em>c<sub>i</sub>v </em>(in that order), we get a linear system of equations <em>At </em>= <em>b</em>, with respect to the unknowns <em>t</em><em>i</em>, <em>i </em>= 1,…, <em>n</em>. Note that the matrix of the system is very sparse; it has at most 3 non-zero entries per row, independently of the size of <em>n</em>. (However, it is not tridiagonal.)

(a) [<em>25 points</em>] Write a MATLAB (or equivalent) script which, for <em>n </em>= 8, 16, 32, 64, generates the matrix and right-hand side vector of the linear system, then solves the linear system (using backslash), and outputs <em>n</em>, the maximum and minimum tension, the acceleration and the condition number of <em>A</em>, using format fprintf(’%3d %10.3e %10.3e %10.3e %10.3e0, …. After the loop of <em>n</em>, the script plots the tension vectors components (not including the acceleration), versus their normalized (by the respective <em>n</em>) index, in one plot (four lines plotted). Do this twice, (i)

<em>i </em>− 1                               <em>i </em>− 1

with <em>v </em>= 6, <em>m<sub>i </sub></em>= 50 + 50 , and <em>c<sub>i </sub></em>= 50 − 20  , and (ii) with <em>v </em>= 6, <em>m<sub>i </sub></em>drawn randomly in the interval (50,100),

<em>n </em>− 1                              <em>n </em>− 1

CSC336                Assignment 2      C. Christara – 2 –

then sorted from smallest to largest, and <em>c<sub>i </sub></em>drawn randomly in the interval (30,50), then sorted from largest to smallest. Use appropriate labels and a legend. In latex, the two plots must be placed side-to-side with captions and subcaptions. At the end of the loop for <em>n</em>, and for the case (i) only, plot in <strong>log-log </strong>scale (loglog) the condition numbers versus <em>n</em>, using a solid line and thick dots for the data (’k.-’). Use appropriate labels.

Based on the numerical results (including plots), comment on how the acceleration and the maximum and minimum tensions behave with <em>n</em>. How do the components of the tension vectors vary with their index? Where (for which <em>i</em>) does the max tension occur? Also comment on how the condition numbers behave with <em>n</em>.

Also outside the loop for <em>n</em>, and for the case (i) and <em>n </em>= 16 only, plot the sparsity patterns of <em>A</em>, <em>P</em>, <em>L</em>,<em>U</em>, in a 2 × 2 format, either using latex or using subplot in matlab. Use appropriate titles and caption. Comment about whether they agree with what you expected. (These comments will be elaborated further in (b).)

<em>Notes</em>: For (i), use m = linspace(50, 100, n)’ and c = 50 – 20*linspace(0, 1, n)’; For (ii), use m = sort(50 + 50*rand(n, 1), ’ascend’); and c = sort(30 + 20*rand(n, 1),

’descend’);

Because the matrix <em>A </em>is sparse, we use sparse matrix techniques to generate it and store it. E.g e = ones(n, 1); A = spdiags([-e, e], [-1, 0], n, n); A(:, n) = -m; Note that you can visualize the sparsity pattern of a sparse matrix <em>A </em>by spy(A).

To get (an estimate of) the condition number of a sparse matrix <em>A</em>, use condest.

If you have four vectors of <em>n<sub>i</sub></em>, <em>i </em>= 1,…,4, components respectively, to plot their components versus their normalized index use plot([1:ni(1)-1]/ni(1), t(1:ni(1)-1, 1), ’r-’, …

[1:ni(2)-1]/ni(2), t(1:ni(2)-1, 2), ’g–’, …

[1:ni(3)-1]/ni(3), t(1:ni(3)-1, 3), ’b-.’, …

[1:ni(4)-1]/ni(4), t(1:ni(4)-1, 4), ’k.’);

<ul>

 <li>[<em>13 points</em>] What would the forms of the <em>L </em>and <em>U </em>factors and of the permutation matrix <em>P </em>be, if LU factorization with row piv oting was applied to the matrix <em>A</em>? Your answer should be given in terms of <em>n </em>and <em>m<sub>i </sub></em>(summation notation is acceptable). Note that this is a mathematical question, but MATLAB could help you get ideas.</li>

 <li>[<em>12 points</em>] Find (mathematically) a closed form formula for the acceleration, and for the tensions <em>t<sub>i</sub></em>, <em>i </em>= 1,…, <em>n </em>− 1, in terms of <em>n</em>, <em>m<sub>i</sub></em>, <em>c<sub>i</sub></em>, <em>v </em>and <em>g</em>. Justify mathematically where (for which <em>i</em>) the maximum tension occurs.</li>

</ul>

1 …, <em>n</em>, <em>j </em>= 1,…, <em>n</em>. The

<ol start="3">

 <li>[<em>35 points</em>] The Hilbert matrix of order <em>n </em>is defined to have entries (<em>H<sub>n</sub></em>)<em><sub>ij </sub></em>= , for <em>i </em>= 1, <em>i </em>+ <em>j </em>− 1</li>

</ol>

Hilbert matrices are known to be very ill-conditioned once <em>n </em>increases beyond a certain value. Use MATLAB (or equivalent) to carry out the following experiments.

(a)       For <em>n </em>= 2,…,13 do the following:

− construct the Hilbert matrix <em>H<sub>n</sub></em>; you may use the built-in MATLAB function hilb(n) or your own function;

<em>n             j</em>

− construct the vector <em>b<sub>n</sub></em>, such that (<em>b<sub>n</sub></em>)<em><sub>i </sub></em>= Σ , for <em>i </em>= 1,…, <em>n</em>; <em>j</em>=<sub>1 </sub><em>i </em>+ <em>j </em>− 1

− solve <em>H<sub>n </sub>x<sub>n </sub></em>= <em>b<sub>n </sub></em>by Gauss elimination; use the backslash  operator to obtain the solution (help slash); let <em>x</em>ˆ<em><sub>n </sub></em>be the computed solution; note that the exact solution is <em>x<sub>n </sub></em>= (1, 2, 3,…, <em>n</em>)<em><sup>T </sup></em>; let <em>r<sub>n </sub></em>= <em>b<sub>n </sub></em>− <em>Hx</em>ˆ<em><sub>n </sub></em>be the residual; − compute the condition number of <em>H<sub>n</sub></em>, the computational relative error ||<em>x<sub>n </sub></em>− <em>x</em>ˆ<em><sub>n</sub></em>|| / ||<em>x<sub>n</sub></em>||, the residual ||<em>r<sub>n</sub></em>||, and ||<em>b<sub>n</sub></em>||, where || ⋅ || is the same norm as that used for the condition number; use the built-in MATLAB functions cond() for computing the condition number of <em>H<sub>n </sub></em>and norm() for computing the norms of vectors (or matrices); (note that both cond() and norm() use Euclidean norms); store the condition number of <em>H<sub>n </sub></em>in the <em>n</em>th component of a vector <em>c</em>, and the respective relative error, norm of residual and of right side vector in the <em>n</em>th component of vectors <em>e</em>, <em>r</em>, <em>v</em>, respectively.

− output <em>n </em>and the four quantities computed above with format fprintf(’%2d %9.2e %9.2e %9.2e

%9.2e
’, …

− Comment on the output and possible warnings by matlab.

(b)     After exiting from the above for-loop,

− In one graph, plot, in semilogy scale, <em>c </em>(the condition number of <em>H<sub>n</sub></em>) versus <em>n</em>, <em>e </em>(||<em>x<sub>n </sub></em>− <em>x</em>ˆ<em><sub>n</sub></em>|| / ||<em>x<sub>n</sub></em>||) versus <em>n</em>, and <em>c</em>(<em>n</em>)<em>r</em>(<em>n</em>)/<em>v</em>(<em>n</em>) versus <em>n</em>. (Thus <em>n </em>will be in the <em>x </em>axis, and will be in regular scale, and the <em>y </em>axis will be in log scale.) To distinguish between the three lines in the plot a solid one for the condition numbers, a dashed line for the relative errors, and a dotted line for the third line. Use appropriate labels and a legend.

− Interpret what you observe in the graph, and discuss whether it agrees with the theory.

<em>Note</em>: You may assume that MATLAB uses double precision. In other language, you must use double precision.

CSC336                                                                               Assignment 2                                    C. Christara