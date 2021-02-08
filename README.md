# Laplace integration method and its precision
A short examination of the precision of the laplace integration method often used in actuarial mathematics in Denmark

I was interested in the question of how good the Laplace integration is at obtaining the actual theoretical values of the integrals.

An theoretical account of the method (in Danish):
http://www.actuar.dk/torben/laplace.pdf

A comparison of the method and the theoretical true value can be found in the jupyter notebook. 
The examples show that the integral is good at handling integrands of polynomial nature if the degree is 5 or less. It is performs less well at larger powers as well as exponential and sine functions.

The examples furthermore considers the integration method when handling a whole life annuity for a person aged x. (This number represents how much money a yearly payment of 1 is worth if the person is x years old and with given assumptions on interest and mortality intensity). It performs resonably when x is zero. However, when we change the x to be a large value, then it performs worse. 

This is exemplified in the following:
For a 100 year old doing the integral from 0 to 120
Theoretical value: 0.007348811477706047
Interval from 0.0 to 120.0
Percentage deviation: 5.11575113186e-06
Absolute deviation: 3.75946906349e-08
Uncertainty in theoretical value: 4.145520167647774e-09

I hypothesise that the reason for this devition is the concentration of the big function-values on few t-values, since the Laplace method is only given values once a year and many values close to zero gives little information on the actual slope of the function.

If you are interested, then you can try your own examples using the code in the nodebook, which for instance can be run for free using Googles colaboratory service directly in the browser.
