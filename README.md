Download Link: https://assignmentchef.com/product/solved-cs161-problem1
<br>
Exercises should be completed <strong>on your own.</strong>

<ol>

 <li><strong> </strong>Have you thoroughly read the course policies on the webpage?</li>

</ol>

<strong>[We are expecting: The answer “yes.”]</strong>

<ol>

 <li><strong> </strong>See the IPython notebook ipynb for Exercise 1. Modify the code to generate a plot that convinces you that <em>T</em>(<em>x</em>) = <em>O</em>(<em>g</em>(<em>x</em>)).<sup>1</sup></li>

</ol>

<strong>[We are expecting: Your choice of </strong><em>c</em><strong>, </strong><em>n</em><sub>0</sub><strong>, the plot that you created after modifying the code in Exercise 1, and a short explanation of why this plot should convince a viewer that </strong><em>T</em>(<em>x</em>) = <em>O</em>(<em>g</em>(<em>x</em>))<strong>.]</strong>

<ol start="2">

 <li><strong> </strong>See the IPython notebook ipynb for Exercise 2, parts A, B and C.

  <ul>

   <li>What is the asymptotic runtime of the function numOnes( lst ) given in the Python notebook? Give the smallest answer that is correct. (For example, it is true that the runtime is <em>O</em>(2<em><sup>n</sup></em>), but you can do better).</li>

  </ul></li>

</ol>

<strong>[We are expecting: Your answer in the form “The running time of </strong>numOnes( lst ) <strong>on a list of size </strong><em>n </em><strong>is </strong><em>O</em>( )<strong>.”, and a few sentences informally justifying why this is the case. ]</strong>

<ul>

 <li>Modify the code in ipynb to generate a picture that backs up your claim from Part (A).</li>

</ul>

<strong>[We are expecting: Your choice of </strong><em>c</em><strong>, </strong><em>n</em><sub>0</sub><strong>, and </strong><em>g</em>(<em>n</em>)<strong>; the plot that you created after modifying the code in Exercise 2; and a short explanation of why this plot should convince a viewer that the runtime of </strong>numOnes <strong>is what you claimed it was.]</strong>

<ul>

 <li>How much time do you think it would take to run numOnes on an input of size <em>n </em>= 10<sup>15</sup>?</li>

</ul>

<strong>[We are expecting: Your answer (in whichever unit of time makes the most sense) with a brief justification, that references the runtime data you generated in part (B). You don’t need to do any fancy statistics, just a reasonable back-of-the-envelope calculation.]</strong>

<ol start="3">

 <li><strong> </strong>Using the definition of big-Oh, formally prove the following statements.</li>

</ol>

√                   √

<ul>

 <li>2 <em>n </em>+ 6 = <em>O</em>( <em>n</em>) (Note that you gave a “proof-by-picture” of this in Exercise 1).</li>

 <li><em>n</em><sup>2 </sup>= Ω(<em>n</em>) (c) log<sub>2</sub>(<em>n</em>) = Θ(ln(<em>n</em>)) (d) 4<em><sup>n </sup></em>is <strong>not </strong><em>O</em>(2<em><sup>n</sup></em>).</li>

</ul>

<strong>[We are expecting: For each part, a rigorous (but short) proof, using the definition of </strong><em>O</em>()<em>,</em>Ω()<strong>, and </strong>Θ()<strong>.]</strong>

<sup>1</sup><strong>Note: </strong>There are instructions for installing Jupyter notebooks in the pre-lecture exercise for Lecture 2.

<h1>Problems</h1>

You may talk with your fellow CS161-ers about the problems. However:

<ul>

 <li>Try the problems on your own <em>before </em></li>

 <li>Write up your answers yourself, in your own words. You should never share your typed-up solutions with your collaborators.</li>

 <li>If you collaborated, list the names of the students you collaborated with at the beginning of each problem.</li>

</ul>

<ol>

 <li>In class we discussed Karatsuba’s algorithm for <em>n</em>-digit integers written in base 10. That is, for an integer <em>x</em>, we wrote , for <em>x<sub>i </sub></em>∈ {0<em>,…,</em>9}. But we can also consider an <em>n</em>-bit integer <em>y </em>written in base 2: , for <em>y<sub>i </sub></em>∈ {0<em>,</em>1}. Or we can think about an <em>n</em>-hexadecimal integer <em>z </em>written in base 16: , for <em>z<sub>i </sub></em>∈{0<em>,…,</em>15}.<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a></li>

</ol>

Your friend has come up with the following argument that integer multiplication can be done in <em>O</em>(1) time. The argument has three parts:

<ul>

 <li>Whatever base we choose to write the numbers out in, Karatsuba’s algorithm correctly findsthe product of those numbers. For example, if we wanted to multiply the numbers 11010011 and 01011010 (which are written in binary), we could do that by recursively performing three multiplications involving the numbers 1101<em>,</em>0011<em>,</em>0101, and 1010.</li>

 <li>For a given number <em>x</em>, the length of <em>x</em>’s base-b representation is decreasing as <em>b </em> For example, the same number <em>x </em>= 1024 (base 10) can be written as

  <ul>

   <li>1000000000 base 2 (10 bits)</li>

   <li>1024 base 10 (4 digits)</li>

   <li>400 base 16 (3 hexits)</li>

  </ul></li>

</ul>

(c) Suppose we want to multiply two numbers <em>x </em>and <em>y</em>. Part (b) means that there’s some largeenough <em>b </em>so that the base-<em>b </em>representations of <em>x </em>and <em>y </em>have length <em>n </em>= <em>O</em>(1). Then we run Karatsuba’s algorithm in this base (which works by part (a)), and it takes time <em>O</em>(<em>n</em><sup>1<em>.</em>6</sup>) = <em>O</em>(1) because <em>n </em>= <em>O</em>(1). Therefore we can multiply any two integers in time <em>O</em>(1).

Unfortunately (from the perspective of fast integer multiplication) your friend’s argument is flawed in at least one place. Which of their steps are faulty and why?

<strong>[We are expecting: For each of (a), (b), and (c), either assert that your friend’s logic is correct, or give a brief argument about why it is wrong. You do not need to give a formal proof in either direction.]</strong>

<ol start="2">

 <li>On an island, there are trustworthy toads and tricky toads. The trustworthy toads always tell the truth; the tricky toads may lie or may tell the truth. The toads themselves can tell who is tricky and who is trustworthy, but an outsider can’t tell the difference: they all just look like toads.</li>

</ol>

You arrive on this island, and are tasked with finding the trustworthy toads. You are allowed to pair up the toads and have them evaluate each other. For example, if Tiffany the Toad and Tom´as the Toad are both Trustworthy Toads, then they will both say that the other is trustworthy. But if Tiffany the Toad is a Trustworthy Toad and Tyrannus the Toad is a Tricky Toad, then Tiffany will call Tyrannus out as tricky, but Tyrannus may say either that Tiffany is tricky or that she is trustworthy. We will refer to one of these interactions as a “toad-to-toad comparison.” The outcomes of comparing toads <em>A </em>and <em>B </em>are as follows:

<table width="407">

 <tbody>

  <tr>

   <td width="87">Toad A</td>

   <td width="87">Toad B</td>

   <td width="116">A says (about B)</td>

   <td width="116">B says (about A)</td>

  </tr>

  <tr>

   <td width="87">Trustworthy</td>

   <td width="87">Trustworthy</td>

   <td width="116">Trustworthy</td>

   <td width="116">Trustworthy</td>

  </tr>

  <tr>

   <td width="87">Trustworthy</td>

   <td width="87">Tricky</td>

   <td width="116">Tricky</td>

   <td width="116">Either</td>

  </tr>

  <tr>

   <td width="87">Tricky</td>

   <td width="87">Trustworthy</td>

   <td width="116">Either</td>

   <td width="116">Tricky</td>

  </tr>

  <tr>

   <td width="87">Tricky</td>

   <td width="87">Tricky</td>

   <td width="116">Either</td>

   <td width="116">Either</td>

  </tr>

 </tbody>

</table>

Suppose that there are <em>n </em>toads on the island, and that there are strictly more than <em>n/</em>2 trustworthy toads.

<em>In this problem, you will develop an algorithm to find all of the trustworthy toads, that only uses O</em>(<em>n</em>) <em>toad-to-toad comparisons. Before you start this problem, think about how you might do this—hopefully it’s not at all obvious! Along the way, you will also practice some of the skills that we’ve seen in Week 1. You will design two algorithms, formally prove that one is correct using a proof by induction, and you will formally analyze the running time of a recursive algorithm.</em>

<ul>

 <li><strong> </strong>Give a straightforward algorithm that uses <em>O</em>(<em>n</em><sup>2</sup>) toad-to-toad comparisons and identifies all of the trustworthy toads.</li>

</ul>

<strong>[We are expecting: A description of the procedure (either in pseudocode or very clear English), with a brief explanation of what it is doing and why it works.]</strong>

<ul>

 <li>Now let’s start designing an improved algorithm. The following procedure will be a building block in our algorithm—make sure you read the requirements carefully!</li>

</ul>

Suppose that <em>n </em>is even. Show that, using only <em>n/</em>2 toad-to-toad comparisons, you can reduce the problem to the same problem with less than half the size. That is, give a procedure that does the following:

<ul>

 <li><strong>Input: </strong>A population of <em>n </em>toads, where <em>n </em>is even, so that there are strictly more than <em>n/</em>2 trustworthy toads in the population.</li>

 <li><strong>Output: </strong>A population of <em>m </em>toads, for 0 <em>&lt; m </em>≤ <em>n/</em>2, so that there are strictly more than <em>m/</em>2 trustworthy toads in the population.</li>

 <li><strong>Constraint: </strong>The number of toad-to-toad comparisons is no more than <em>n/</em></li>

</ul>

<strong>[We are expecting: A description of this procedure (either in pseudocode or very clear English), and rigorous argument that it satisfies the Input, Output, and Constraint requirements above.]</strong>

<ul>

 <li><strong>[This problem is NOT REQUIRED, but you may assume it for future parts.] </strong>Extend your argument for odd <em>n</em>. That is, given a procedure that does the following:

  <ul>

   <li><strong>Input: </strong>A population of <em>n </em>toads, where <em>n </em>is odd, so that there are strictly more than <em>n/</em>2 trustworthy toads in the population.</li>

   <li><strong>Output: </strong>A population of <em>m </em>toads, for 0 <em>&lt; m </em>≤d<em>n/</em>2e, so that there are strictly more than <em>m/</em>2 trustworthy toads in the population.</li>

   <li><strong>Constraint: </strong>The number of toad-to-toad comparisons is no more than b<em>n/</em></li>

  </ul></li>

</ul>

(<em>?</em>) <em>For all of the following parts, you may assume that the procedures in parts (b) and (c) exist even if you have not done those parts.</em>

<ul>

 <li><strong>(1 pt.) </strong>Using the procedures from parts (b) and (c), design a recursive algorithm that uses <em>O</em>(<em>n</em>) toad-to-toad comparisons and finds a <em>single </em>trustworthy toad.</li>

</ul>

<strong>[We are expecting: A description of the procedure (either in pseudocode or very clear English). ]</strong>

<ul>

 <li><strong> </strong>Prove formally, using induction, that your answer to part (d) is correct.</li>

</ul>

<strong>[We are expecting: A formal argument by induction. Make sure you explicitly state the inductive hypothesis, base case, inductive step, and conclusion.]</strong>

<ul>

 <li>Prove that the running time of your procedure in part (d) uses <em>O</em>(<em>n</em>) toad-to-toad comparisons.</li>

</ul>

<strong>[We are expecting: A formal argument. Note: do this argument “from scratch,” do not use the Master Theorem.]</strong>

<ul>

 <li>Give a procedure to find <em>all </em>trustworthy toads using <em>O</em>(<em>n</em>) toad-to-toad comparisons.</li>

</ul>

<strong>[We are expecting: An informal description of the procedure. ]</strong>

<a href="#_ftnref1" name="_ftn1">[1]</a> You may be used to representing number in hex on a computer, where it doesn’t use symbols 0<em>,…,</em>15 but rather 0<em>,…,</em>9, along with the symbols <em>A,B,C,D,E,F</em>. In fact, this is the same thing, we just read “A” as 10, ”B” as 11, and so on. So in hex, 1<em>AF </em>= 1 · 16<sup>2 </sup>+ 10 · 16<sup>1 </sup>+ 15 · 16<sup>0 </sup>= 431 base 10.

<a href="#_ftnref2" name="_ftn2">[2]</a> This is the trickiest part of the problem set! You may have to think a while.