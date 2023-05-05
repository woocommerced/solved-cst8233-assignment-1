Download Link: https://assignmentchef.com/product/solved-cst8233-assignment-1
<br>
Catenary Function

<strong>Purpose:</strong> Investigate a Maclaurin series approximation to the Catenary function.  <strong>Algorithm </strong>

Write a program named <em>ass1</em> that will enable the user to generate a Maclaurin series approximation to the Catenary function that is important in engineering and Nature in general. It is the shape a simple necklace hangs in round your neck or the shape of a lightweight suspension bridge or the strands of a spider’s web. It is also a function widely used in architecture:







In this assignment we imagine that an architecture company wishes to code a real-time simulation walkthrough that includes a Catenary Arch (as shown above). To do this they are prepared to implement the Catenary function by a fast but approximate Maclaurin series instead of slower but more accurate math library functions. Your assignment will investigate the accuracy of the series approximation to this function.







The catenary function (the inverted arch) is a hyperbolic cosine function that can be written as a combination of exponentials :










The graph at right shows f(x) = y as the vertical axis and x as the horizontal axis. <em>a</em> is a scale factor. Increasing the value

of <em>a</em> is equivalent to magnifying the curve, but not changing <a href="https://en.wikipedia.org/wiki/File:Catenary-pm.svg"><sup> </sup></a>its shape. In this assignment you can think of <em>a</em> as a parameter to increase the length of the Catenary or increase the separation of its ends.




In this assignment you will write a Maclaurin series expansion of the Catenary function that goes up to and including the term in x<sup>12</sup>. The purpose of the series approximation is to speed up its execution so math library function (such as exp() or pow() or any other) are not used in the evaluation of the terms of the series and terms such as x<sup>3</sup> are written explicitly in your code as x*x*x.




<strong>Algorithm: </strong>While the user wishes to continue, the integer value of the highest power of x in the series is selected (you should reject invalid integers). Then the user selects a range of x, somewhere between 10.0 and +10.0 over which the series is evaluated from 0 in ten equal increments (you should reject values outside this range). Then the user chooses the value of the scale factor <em>a</em>.




For each value of x the Maclaurin series approximation to the Catenary function is output together with the exact value calculated from the math library using the exp() function.

The error that results from using the series approximation is calculated in two different ways.




<ol>

 <li>From comparison with the exact value calculated using the math library cosh() function: Exact % Error = 100*(exact value – series value)/exact value</li>

</ol>




<ol start="2">

 <li>From the first truncated term. This gives you an idea of how well the first truncated term approximates to the error.</li>

</ol>

Truncation % Error = 100*first truncated term/series value.




Set up a Win32 console project in Visual Studio 2015 with the name ass1. Write the code to implement the application, as described above, in a file named ass1.cpp using the C (or/C++) programming language.

Example output is given at the end. Yours should be very similar, but may differ very slightly due to roundoff errors from the way you have evaluated your series. Note than your assignment might be tested with different parameters than those shown.




See the Marking Sheet for how you can lose marks, but you definitely lose 60% or more if: l         the series is wrong <strong> </strong>

<ul>

 <li>Your application won’t build in Visual Studio 2015</li>

 <li>Your application crashes in normal operation</li>

 <li>I can’t build it because you submitted the wrong files or the files are missing, even if it’s an honest mistake – 100% deduction.</li>

</ul>

<strong> </strong>

<strong>What to Submit :</strong> Use Blackboard to submit this assignment as a zip file (<strong>not </strong>RAR, not 9zip, not 7 zip) containing only the source code file (ass1.cpp). The name of the zipped folder <strong><u>must </u></strong>contain your name as a prefix so that I can identify it, for example using my name the file would be tyleraAss1CST8233.zip. It is also vital that you include the Cover Information (as specified in the Submission Standard) as a file header in your source file so the file can be identified as yours. Use comment lines in the file to include the header.

There is a late penalty of 25% per day – even one minute is counted late. Don’t send me the file as an email attachment – it will get 0.




Example Output

**********************************

Catenary Series

<ol>

 <li>Evaluate the function</li>

 <li>Quit</li>

</ol>

**********************************

1




EVALUATING THE CATENARY SERIES APPROXIMATION

Please enter the highest power of x in the catenary series (0, 2, 4, 6, 8, or 10): 8




<h2><a name="_Toc8452"></a>        CHOOSE THE RANGE OF EVALUATION – low x to high x</h2>

Please enter low x – in the range -10.0 to 0.0: -2

<h1><a name="_Toc8453"></a>Please enter high x – in the range 0.0 to +10.0: 2</h1>




<h1><a name="_Toc8454"></a>Please enter the scale factor the range 0.0 to +10.0: 1</h1>




CATENARY SERIES TO x^8 from x = -2.000000 to x = 2.000000

x          Series         Exact         Exact % Error    Trunc. % Error -2.000e+00   3.76190e+00   3.76220e+00      7.73296e-03      7.50117e-03

-1.600e+00   2.57743e+00   2.57746e+00      1.19868e-03      1.17557e-03

-1.200e+00   1.81065e+00   1.81066e+00      9.52715e-05      9.42354e-05

-8.000e-01   1.33743e+00   1.33743e+00      2.22317e-06      2.21240e-06

-4.000e-01   1.08107e+00   1.08107e+00      2.67613e-09      2.67290e-09

+0.000e+00   1.00000e+00   1.00000e+00      0.00000e+00      0.00000e+00

+4.000e-01   1.08107e+00   1.08107e+00      2.67615e-09      2.67290e-09

+8.000e-01   1.33743e+00   1.33743e+00      2.22317e-06      2.21240e-06

+1.200e+00   1.81065e+00   1.81066e+00      9.52715e-05      9.42354e-05

+1.600e+00   2.57743e+00   2.57746e+00      1.19868e-03      1.17557e-03

+2.000e+00   3.76190e+00   3.76220e+00      7.73296e-03      7.50117e-03




**********************************

Catenary Series

<ol>

 <li>Evaluate the function</li>

 <li>Quit</li>

</ol>

**********************************

1




EVALUATING THE CATENARY SERIES APPROXIMATION




Please enter the highest power of x in the catenary series (0, 2, 4, 6, 8, or 10): 10




CHOOSE THE RANGE OF EVALUATION – low x to high x

Please enter low x – in the range -10.0 to 0.0: -4

Please enter high x – in the range 0.0 to +10.0: 2




Please enter the scale factor the range 0.0 to +10.0: 2




CATENARY SERIES TO x^10 from x = -4.000000 to x = 2.000000   x          Series         Exact         Exact % Error    Trunc. % Error -4.000e+00   7.52437e+00   7.52439e+00      2.32370e-04      2.27291e-04

-3.400e+00   5.65663e+00   5.65663e+00      4.36965e-05      4.30053e-05

-2.800e+00   4.30180e+00   4.30180e+00      5.56249e-06      5.50275e-06

-2.200e+00   3.33704e+00   3.33704e+00      3.95309e-07      3.92685e-07

-1.600e+00   2.67487e+00   2.67487e+00      1.07646e-08      1.07268e-08

-1.000e+00   2.25525e+00   2.25525e+00      4.52507e-11      4.51916e-11

-4.000e-01   2.04013e+00   2.04013e+00      0.00000e+00      0.00000e+00

+2.000e-01   2.01001e+00   2.01001e+00      0.00000e+00      0.00000e+00

+8.000e-01   2.16214e+00   2.16214e+00      3.22467e-12      3.24521e-12

+1.400e+00   2.51034e+00   2.51034e+00      2.30839e-09      2.30218e-09

+2.000e+00   3.08616e+00   3.08616e+00      1.36039e-07      1.35293e-07




**********************************

Catenary Series

<ol>

 <li>Evaluate the function</li>

 <li>Quit</li>

</ol>

**********************************

1




EVALUATING THE CATENARY SERIES APPROXIMATION




Please enter the highest power of x in the catenary series (0, 2, 4, 6, 8, or 10): 2




CHOOSE THE RANGE OF EVALUATION – low x to high x

Please enter low x – in the range -10.0 to 0.0: -10 Please enter high x – in the range 0.0 to +10.0: 2




Please enter the scale factor the range 0.0 to +10.0: 10




CATENARY SERIES TO x^2 from x = -10.000000 to x = 2.000000   x          Series         Exact         Exact % Error    Trunc. % Error -1.000e+01   1.50000e+01   1.54308e+01      2.79186e+00      2.77778e+00

-8.800e+00   1.38720e+01   1.41284e+01      1.81488e+00      1.80128e+00

-7.600e+00   1.28880e+01   1.30297e+01      1.08762e+00      1.07859e+00

-6.400e+00   1.20480e+01   1.21189e+01      5.84762e-01      5.80221e-01

-5.200e+00   1.13520e+01   1.13827e+01      2.70067e-01      2.68367e-01

-4.000e+00   1.08000e+01   1.08107e+01      9.91952e-02      9.87654e-02

-2.800e+00   1.03920e+01   1.03946e+01      2.47030e-02      2.46446e-02

-1.600e+00   1.01280e+01   1.01283e+01      2.69838e-03      2.69616e-03

-4.000e-01   1.00080e+01   1.00080e+01      1.06587e-05      1.06581e-05

+8.000e-01   1.00320e+01   1.00320e+01      1.70158e-04      1.70122e-04

+2.000e+00   1.02000e+01   1.02007e+01      6.54424e-03      6.53595e-03




**********************************

Catenary Series

<ol>

 <li>Evaluate the function</li>

 <li>Quit</li>

</ol>

**********************************

1




EVALUATING THE CATENARY SERIES APPROXIMATION




Please enter the highest power of x in the catenary series (0, 2, 4, 6, 8, or 10): 6




<a href="#_Toc8452">        CHOOSE THE RANGE OF EVALUATION – low x to high x Please enter low x – in the range -10.0 to 0.0:                                                   1 </a>

<a href="#_Toc8453">Please enter high x – in the range 0.0 to +10.0:                                                                                                           1 </a>

<a href="#_Toc8454">Please enter the scale factor the range 0.0 to +10.0: 0                                                                                                    1 </a>










CATENARY SERIES TO x^6 from x = -1.000000 to x = 1.000000   x          Series         Exact         Exact % Error    Trunc. % Error -1.000e+00   1.85656e+02   1.10132e+03      8.31425e+01      1.33589e+02

-8.000e-01   5.67756e+01   1.49048e+02      6.19079e+01      7.32889e+01

-6.000e-01   1.37800e+01   2.01716e+01      3.16860e+01      3.02301e+01

-4.000e-01   2.53556e+00   2.73082e+00      7.15051e+00      6.41042e+00

-2.000e-01   3.75556e-01   3.76220e-01      1.76496e-01      1.69062e-01

+0.000e+00   1.00000e-01   1.00000e-01      0.00000e+00      0.00000e+00

+2.000e-01   3.75556e-01   3.76220e-01      1.76496e-01      1.69062e-01

+4.000e-01   2.53556e+00   2.73082e+00      7.15051e+00      6.41042e+00

+6.000e-01   1.37800e+01   2.01716e+01      3.16860e+01      3.02301e+01

+8.000e-01   5.67756e+01   1.49048e+02      6.19079e+01      7.32889e+01

+1.000e+00   1.85656e+02   1.10132e+03      8.31425e+01      1.33589e+02




**********************************

Catenary Series

<ol>

 <li>Evaluate the function</li>

 <li>Quit</li>

</ol>

**********************************