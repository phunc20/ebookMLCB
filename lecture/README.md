
```python
from cvxopt import matrix, solvers
P = matrix([[1., 0.], [0., 1.]])
P
PP = matrix([[1, 0], [0, 1]])
PP
P.tc
dir(P)
%history
q = matrix([-10., -10.])
help(solver.qp)
help(solvers.qp)
%history

In [13]: G = matrix([[1., 1.], [2., 1.], [1., 4.], [-1., 0.], [0., -1.]])

In [14]: G
Out[14]: <2x5 matrix, tc='d'>

In [15]: help(matrix)


In [16]: h = matrix([10., 16., 32., 0., 0.])

In [17]: h = matrix([10., 16., 32., 0., 0])

In [18]:

In [18]: h
Out[18]: <5x1 matrix, tc='d'>

In [19]: h = matrix([10., 16, 32, 0, 0])
In [21]: sol = solvers.qp(P, q, G, h)
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
<ipython-input-21-39028ce32805> in <module>
----> 1 sol = solvers.qp(P, q, G, h)

~/.virtualenvs/py3.7/lib/python3.7/site-packages/cvxopt/coneprog.py in qp(P, q, G, h, A, b, solver,
kktsolver, initvals, **kwargs)
   4483             'residual as dual infeasibility certificate': dinfres}
   4484
-> 4485     return coneqp(P, q, G, h, None, A,  b, initvals, kktsolver = kktsolver, options = option
s)

~/.virtualenvs/py3.7/lib/python3.7/site-packages/cvxopt/coneprog.py in coneqp(P, q, G, h, dims, A, b
, initvals, kktsolver, xnewcopy, xdot, xaxpy, xscal, ynewcopy, ydot, yaxpy, yscal, **kwargs)
   1893         if G.typecode != 'd' or G.size != (cdim, q.size[0]):
   1894             raise TypeError("'G' must be a 'd' matrix of size (%d, %d)"\
-> 1895                 %(cdim, q.size[0]))
   1896         def fG(x, y, trans = 'N', alpha = 1.0, beta = 0.0):
   1897             misc.sgemv(G, x, y, dims, trans = trans, alpha = alpha,

TypeError: 'G' must be a 'd' matrix of size (5, 2)
In [13]: G = matrix([[1., 1.], [2., 1.], [1., 4.], [-1., 0.], [0., -1.]])

In [14]: G
Out[14]: <2x5 matrix, tc='d'>
In [26]: import numpy as np

In [27]: G = np.array([[1., 1.], [2., 1.], [1., 4.], [-1., 0.], [0., -1.]])

In [28]: G.shape
Out[28]: (5, 2)

In [29]: matrix(G)
Out[29]: <5x2 matrix, tc='d'>
```
