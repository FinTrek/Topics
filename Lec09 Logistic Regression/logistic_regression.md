Intro to Logistic Regression and OkCupid Data
========================================================
author: Albert Y. Kim
date: Wednesday 2015/03/9






Binary Outcome Variables
========================================================

Let out outcomes be **binary**.  

i.e. for $i=1, \ldots, n$ observations

* $y_i = 1$ if some condition holds
* $y_i = 0$ if some condition does not hold

We're interested in $p_i = \mbox{Pr}(y_i = 1)$.



Logistic Regression
========================================================

Logistic regression is preferred over linear regression here because you might end up with fitted probabilities $\widehat{p}_i = \widehat{\mbox{Pr}}(y_i = 1)$ that are either

* less than 0
* greater than 1

So we use the not the first model, but the second:

$$
\begin{eqnarray}
p_i &=& \beta_1 X_{i1} + \ldots  + \beta_k X_{ik}\\
\mbox{logit}(p_i)=\log\left(\frac{p_i}{1-p_i}\right) &=& \beta_1 X_{i1} + \ldots  + \beta_k X_{ik}
\end{eqnarray}
$$


OkCupid Data
========================================================
Result of a Python script that scraped the OkCupid website.  We consider 59K users who were

* members on 2012/06/26
* within 25 miles of SF
* online in the last year
* have at least one photo

Their public profiles were pulled on 2012/06/30.  i.e. only data that’s visible to the public



OkCupid Data
========================================================

* essay0- My self summary
* essay1- What I’m doing with my life
* essay2- I’m really good at
* essay3- The first thing people usually notice about me
* essay4- Favorite books, movies, show, music, and food




OkCupid Data
========================================================

* essay5- The six things I could never do without
* essay6- I spend a lot of time thinking about
* essay7- On a typical Friday night I am
* essay8- The most private thing I am willing to admit
* essay9- You should message me if...




Questions
========================================================

* Knowing nothing about a user, what is your best guess of the probability that the user is female?
* Is height predictive of a user's sex?
* Is the use of the word "wine" in a user's essay questions predictive of ...




Acknowledgements
========================================================

Thanks to Christian Rudder from OkCupid and OkTrends for agreeing to the data's use.

Journal of Statistics Education paper can be found [here](https://github.com/rudeboybert/JSE_OkCupid).


