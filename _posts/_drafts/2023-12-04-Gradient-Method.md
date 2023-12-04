---
title: Gradient Method
categories:
  - Machine Learing
feature_text: |
  Introduce gradient method frequantly used in machine learning with python.
excerpt: |
  Gradient method is way to find local minimum or maximum. This method used in machine learning to find parameter minimize the error function.
---
# Gradient
This part is not intended to explain gradient deeply. Just brief what it is and check what we need to use gradient method.

The definition of gradient is
$$df = \nabla f \cdot d \mathbf r$$
I interpret this : space-wise differentiation or general version of differentiation in spacial manner.

Thinking 1D:

$$df = \frac{d f}{d x}dx$$

which is just same as:
$$df = \frac{\partial f}{\partial x}dx \hat x$$

Because there is only independent value x.

How it would be in 3D? There are three independent variable x, y, z. We can make a function f and define the gradient:

$$df = \frac{\partial f}{\partial x}fdx\hat x+\frac{\partial f}{\partial x}fdy\hat y+\frac{\partial f}{\partial x}fdz\hat z$$



# Gradient Method
I will explain the gradient descent method which is finding the minimum of function. The gradient ascent method is just opposite, finding the maximum and quite same way.

The minimum of error function is where machine learning want to find. The minimum point means that we are now have optimal parameters.

For now, think two independent variables(2D space) and function z: $$z = z(x,y)$$, z is not independent variable in this time, it depends on x and y.
And we can make 3D plot with this.

There is four cases where the gradient is zero: the local minimum, the local maximum, the saddle point, flat point.
The saddle point is where minimize in one independent variable, but maximize another. The shape of the saddle point is like the saddle of horse or the back of arabian camel. If we watch the camel from side: it looks local minimum. How about front view?, we just can see the face of camel, so you have to imagine: how about the point where we saw local minimum? The point is now local maximum.
There is flat area, where by x or y, z is not changed. This makes it hard to find minimum point, and that why we should use good error function.

So how the gradient method works? In coding convention:
$$x = x - \eta \frac{\partial f}{\partial x}$$
$$y = y - \eta \frac{\partial f}{\partial y}$$

or we can use subscript on x and y with n+1 and n each.

By using this equation, or exactly replacement, we can finding next value which  going opposite direction of gradient vector, and maybe better if the method worked well.

Look the definition of gradient above again, it is actually vector, pointing where increasing the function. Its opposite direction is, therefore, where decreases the function, z this time. It means if we 'move' to next value x and y slightly toward opposite direction of gradient, the function z decreases.

But there are bad cases: 'missing' the minimal point because we set $$\eta$$ too big, or finding local minimum not global minimum and 'trapped' this minimum because we set $$\eta$$ too small to escape the local minimum

The next value might not be a better one. If we go too far so that we just 'missed' the minimal point.

Or we might find a minimum point but it is local and there is point having smaller z. And we just can't get there because we can't go out this hole like we 'trapped'. There is another cause of this problem: starting point. If we start near the global minimum, we could find the minimum point. But if near wrong hole, which is local but global minimum, we then trapped.

How we then manage length of each step? There is $$\eta$$ in the replacing equation. We can set $$\eta$$ big or small to go each step big or small.
