#### Python Day 5:

#### **Linear Optimization problem **

*Side Story:  Excel Solver is an excellent tool for Linear Optimization problems, but we need to pay for this platform.*
*In addition, 5 asked me with an extremely surprised facial expression: "**What kind of data scientists would use Excel**? "* 😱😱😱

Therefore we will introduce how to use Python to solve a Linear Optimization Problem, so we can all be Real data Scientists.

#### **Problem:**

Pirelli glass produces two types of fiber optic strands: A-type & H-type (a higher speed variety).

            A-type           H-type

Fiber  1                    1

Labor  9 hours        6 hours 

Glass  12 lbs            16 lbs

Unit Profit  350usd      300usd

Due to an unusual agreement they made as part of a takeover of a small company next week they are only allowed to produce 200 fibers, there are 1566 hours of labor available, and 2880 lbs of glass available.

#### **Question:**

We want to determine the **best combination of A-type and H-type fibers** to produce?

[caption id="attachment_1564" align="alignnone" width="750"]![image](http://upload-images.jianshu.io/upload_images/8699364-c6f0f5c3c7073474.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

 [pixel2013](https://pixabay.com/users/pixel2013/) / Pixabay[/caption]

**Solution Key:**

X1=number of A-type fibers to produce
X2=number of H-type fibers to produce

***MAX Revenue*** :  $F(x) = 350X1 + 300X2$

***Constrain:***

$1X1 + 1X2 <= 200$ fibers
$9X1 + 6X2 <= 1566$ labor
$12X1 + 16X2 <= 2880$ glass
$X1 >= 0$
$X2 >= 0$

**Python Code:**
``` python
from scipy.optimize import linprog 
import numpy as np
import matplotlib.pyplot as plt
from numpy.linalg import solve
%matplotlib inline

# Solve
#Note linprog is for min, in order to solve for max, 
#we switch the sign
c=[-350, -300]
A=[[1,1],[9,6],[12,16]]
b=[200,1566,2800]
x0_bounds=(0,None)
x_bounds=(0,None)

res = linprog(c, A_ub=A, b_ub=b, bounds=(x0_bounds, x_bounds))

print(res)
```

**Output:**

Remember the Trickest point to solve this problem is 
**Min(f(x))= -(Max(f(x))) ⇔ Max(f(x))= -(Min(f(x)))**

Therefore we have our ***Max Profit = 66100 with A-type fibers=122 and B-type fibers=78***
```
  fun: -66100.0
 message: 'Optimization terminated successfully.'
     nit: 2
   slack: array([  0.,   0.,  88.])
  status: 0
 success: True
       x: array([ 122.,   78.])
```

**Visualization:**

![image](http://upload-images.jianshu.io/upload_images/8699364-7d7ae29c0412e00e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

**Python Code:**

```
x= np.linspace(0,200,2000)
y1=200-x
y2=(1566-6*x)/9
y3=(2880-16*x)/12

plt.plot(x, y1, label=r'$y\leq 200-x /pre>)
plt.plot(x, y2, label=r'$9y\leq1566- 6x/pre>)
plt.plot(x, y3, label=r'$12y\leq2880  - 16x/pre>)

plt.xlim((0, 200))
plt.ylim((0, 200))
plt.xlabel(r'$x/pre>)
plt.ylabel(r'$y/pre>)

# Fill feasible region
y5 = np.minimum( y1, y2 )
y6 = np.minimum(y2, y3)
y7= np.minimum(y5,y6)
plt.fill_between(x,y7, color='grey', alpha=0.5)
plt.legend(bbox_to_anchor=(1.05, 1), loc=2, borderaxespad=0.)

plt.show()
```

**Reference:**

Bellur Srikar, HU ANLY 705, Linear Optimization Lecture notes
[http://www.vision.ime.usp.br/~igor/articles/optimization-linprog.html](http://www.vision.ime.usp.br/~igor/articles/optimization-linprog.html)

[http://benalexkeen.com/linear-programming-with-python-and-pulp-part-1/](http://benalexkeen.com/linear-programming-with-python-and-pulp-part-1/)

[https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.linprog.html](https://docs.scipy.org/doc/scipy/reference/generated/scipy.optimize.linprog.html)

##### **Happy Studying!!!** 🤭
