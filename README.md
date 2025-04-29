# cs111-homework-3-solved
**TO GET THIS SOLUTION VISIT:** [CS111 Homework 3 Solved](https://www.ankitcodinghub.com/product/cs111-submit-your-paper-as-one-pdf-file-and-tell-gradescope-which-pages-each-problem-is-on-if-you-worked-with-a-partner-you-must-each-turn-in-your-own-homework-paper-and-report-the-name-and-pe-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;115128&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS111 Homework 3 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
1. Consider the code for the temperature problem in the file cs111/temperature.py, especially the routine make b() that creates the right-hand side b. Let k = 100.

1.1. How many elements are there in b?

1.2. Considering all possible choices for the temperatures on the boundary, what is the smallest number of elements of b that could possibly be nonzero? Explain why in English.

1.3. Considering all possible choices for the temperatures on the boundary, what is the largest number of elements of b that could possibly be nonzero? Explain why in English.

2. The temperature problem models our cabin in the woods in two dimensions, but most modern scientific simulations are done in three dimensions. Here you will create the matrix that corresponds to a 3-D version of the temperature problem. The “cabin” is now the unit cube. As before, we will discretize the interior by dividing it into k points in each dimension, but now there are a total of k3 points rather than k2.

The partial differential equation still leads to the approximation that the temperature at any given point is the average of the temperatures at the neighboring points, but now there are 6 neighbors, with 2 in each of the three dimensions. The matrix A for the 3D version of the temperature problem expresses the fact that, in a 3D k-by-k-by-k grid, each interior point has a temperature that is the average of its 6 neighbors (left, right, up, down, in, out). The diagonal elements of A are all equal to 6, and the off-diagonal elements are either 0 or −1. Most of the rows of A have 7 nonzeros.

Using make A(k) from cs111/temperature.py as a model, write a routine make A 3D(k) that returns the k3-by-k3 matrix A. Like make A(k), your routine should create A as a sparse matrix using scipy.sparse.csr matrix(), after making a table “triples” of the nonzero elements of A.

Here below, for your debugging, is the correct matrix for k = 2. I converted it to a dense array for printing—you should also print it out as a sparse matrix (that line is commented out below), and indeed for k &gt; 2 it’s going to be too large to see what’s going on in the dense matrix anyway.

[In:]

k = 2

A = make_A_3D(k) print(’k:’, k) print(’dimensions:’, A.shape) print(’nonzeros:’, A.nnz) #print(’A as sparse matrix: ’, A) print(’A as dense matrix: ’, A.toarray())

[Out:] k: 2

dimensions: (8, 8) nonzeros: 32

A as dense matrix:

[[ 6. -1. -1. 0. -1. 0. 0. 0.]

[-1. 6. 0. -1. 0. -1. 0. 0.]

[-1. 0. 6. -1. 0. 0. -1. 0.]

[ 0. -1. -1. 6. 0. 0. 0. -1.]

[-1. 0. 0. 0. 6. -1. -1. 0.]

[ 0. -1. 0. 0. -1. 6. 0. -1.]

[ 0. 0. -1. 0. -1. 0. 6. -1.]

[ 0. 0. 0. -1. 0. -1. -1. 6.]]

To complete a realistic simulation you would also write a routine make b 3D(k) to compute the right-hand side b. For this problem, you don’t have to do that.

3. Do problem 2.3 on pages 32–33 of Chapter 2 of the NCM book, showing the numpy code you use and its output. Note: To understand intuitively what the problem means by “assume that joint 1 is rigidly fixed both horizontally and vertically and that joint 8 is fixed vertically,” think of the truss as a (2-dimensional) drawbridge across a river, with the left end being a hinge and the right end lying on the ground.

4. The condition number of a matrix A is a measure of how close to being singular it is. The definition is κ(A) = ||A|| ||A−1||,

with the convention κ(A) = ∞ if A is singular. Each different matrix norm gives its own definition of condition number; usually we’ll consider the 2-norm condition number. The condition number is always at least 1. (I’ll prove that in class.) A matrix is well-conditioned if its condition number is not too big (think 103 or less), and ill-conditioned if its condition number is very large (think 106 or more). In numpy, the condition number is computed by npla.cond().

In this problem you’ll explore the relationship between condition number and the behavior of LU factorization.

4.1. Consider the linear system

,

for some α &lt; 1. Clearly the solution is (x0,x1)T = (−1,1)T.

For each value of α = 10−4, 10−8, 10−16, 10−20, try to solve this system twice, using the routine cs111.LUsolve(), first with pivoting = True and then with pivoting = False. For each solution, print: the condition number of A; the computed x; the norm of the error; and the relative residual norm returned by cs111.LUsolve(). Show your numpy code and its output.

As α decreases, does A become ill-conditioned or does it remain well-conditioned? Describe and explain the trends in the relative residual norm for both the non-pivoting and pivoting solutions. 4.2. Consider the linear system

,

for some α &lt; 1. Again, the solution is (x0,x1)T = (−1,1)T.

For each value of α = 10−4, 10−8, 10−16, 10−20, try to solve this system twice, using the routine cs111.LUsolve(), first with pivoting = True and then with pivoting = False. This time, some of the tries will fail to return an answer. For each try, print the condition number of A. If an answer was returned, print: the computed x; the norm of the error; and the relative residual norm returned by cs111.LUsolve(). Show your numpy code and its output.

As α decreases, does A become ill-conditioned or does it remain well-conditioned? Describe and explain the trends in the relative residual norm for the successful tries. Explain why the other tries were unsuccessful.
