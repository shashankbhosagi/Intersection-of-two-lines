# Visualizing Intersection of two point in Javascript.

### Given the coordinates of points of line, how to find the intersection of points.

#### Let there be two lines namely `AB` and `CD` with coordintes `(Ax,Ay)` , `(Bx,By)`, `(Cx,Cy)` , `(Dx,Dy)` respectively...
#### Let they both intersect a point `I (Ix, Iy)`.
```
Ix = Ax + (Bx-Ax)t = Cx + (Dx-Cx)u
Iy = Ay + (By-Ay)t = Cy + (Dy-Cy)u
```
### We have to now find t or u to get solution ;)
```
Ax + (Bx-Ax)t = Cx + (Dx-Cx)u
(Ax-Cx) + (Bx-Ax)t = (Dx-Cx)u ----(1)
```
```
Ay + (By-Ay)t = Cy + (Dy-Cy)u
(Ay-Cy) + (By-Ay)t = (Dy-Cy)u ----(2)
```
Multiplying (2) by (Dx-Cx) on B.S

(Ay-Cy)*(Dx-Cx) + (By-Ay)*(Dx-Cx)t = (Dy-Cy)*(Dx-Cx)*u

#### Substituting value of (Dx-Cx)*u from (1)
```
(Ay-Cy)*(Dx-Cx) + (By-Ay)*(Dx-Cx)t = (Dy-Cy)*[(Ax-Cx) + (Bx-Ax)t]
```
#### SOlving the brackets on RHS
```
(Ay-Cy)*(Dx-Cx) + (By-Ay)*(Dx-Cx)t = (Dy-Cy)*(Ax-Cx) + (Dy-Cy)*(Bx-Ax)t

```
#### Substracting (Dy-Cy)*(Ax-Cx) & (By-Ay)*(Dx-Cx)t on both sides

```
(Ay-Cy)*(Dx-Cx) - (Dy-Cy)*(Ax-Cx) + (By-Ay)*(Dx-Cx)t =(Dy-Cy)*(Bx-Ax)t
(Ay-Cy)*(Dx-Cx) - (Dy-Cy)*(Ax-Cx) =(Dy-Cy)*(Bx-Ax)-t(By-Ay)*(Dx-Cx)t

```
#### Taking t as a factor on RHS
```
(Ay-Cy)*(Dx-Cx) - (Dy-Cy)*(Ax-Cx) =[(Dy-Cy)*(Bx-Ax)-(By-Ay)*(Dx-Cx)]*t

```
#### Dividing the eq with (Dy-Cy)*(Bx-Ax)-(By-Ay)*(Dx-Cx) on B.S
```
[(Ay-Cy)*(Dx-Cx) - (Dy-Cy)*(Ax-Cx)] / [(Dy-Cy(Bx-Ax) -(By-Ay)*(Dx-Cx)] = t

```

#### Similarly solving for u we get 
```
[(Cy-Ay)*(Ax-Bx) - (Cx-Ax)*(Ay-By)] / [(Dy-Cy(Bx-Ax) -(By-Ay)*(Dx-Cx)] = u
```

Now we can substitute the value of `t` or `u` in Ix and Iy equation to get the value of I which is intersection point.


### COde

The HTML code contains a visualization in which line `AB` is rotating and `CD` line is stationary and we can see how the point will look like on the line. THis will help me visualize the point I when getting intersected.

I have also handled edge cases such as 
- If the denominator of `t` equation is equal to zero then it means that lines are parallel to each other means there is no single point of intersection between them.
- As we are using line interpolation to get points `t` and `u` it may go out of bond `[0,1]` then it would show outiside points also so I have also handeled them by limit the value of both `t` and `u` in between 0 and 1.
    
