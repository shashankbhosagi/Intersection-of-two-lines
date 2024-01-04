#Visualizing Intersection of two point in Javascript.

Given the coordinates of points of line, how to find the intersection of points.

let there be two lines namely AB and CD with coordintes (Ax,Ay) , (Bx,By) , (Cx,Cy) , (Dx,Dy) respectively...
let they both intersect a point I(Ix, Iy).

Ix = Ax + (Bx-Ax)t = Cx + (Dx-Cx)u
Iy = Ay + (By-Ay)t = Cy + (Dy-Cy)u

We have to now find t or u to get solution ;)

Ax + (Bx-Ax)t = Cx + (Dx-Cx)u
(Ax-Cx) + (Bx-Ax)t = (Dx-Cx)u ----(1)

Ay + (By-Ay)t = Cy + (Dy-Cy)u
(Ay-Cy) + (By-Ay)t = (Dy-Cy)u ----(2)

Multiplying (2) by (Dx-Cx) on B.S

(Ay-Cy)_(Dx-Cx) + (By-Ay)_(Dx-Cx)t = (Dy-Cy)*(Dx-Cx)*u

    substituting value of (Dx-Cx)*u from (1)

(Ay-Cy)_(Dx-Cx) + (By-Ay)_(Dx-Cx)t = (Dy-Cy)_[(Ax-Cx) + (Bx-Ax)t]
(Ay-Cy)_(Dx-Cx) + (By-Ay)_(Dx-Cx)t = (Dy-Cy)_(Ax-Cx+ (Dy-Cy)_(Bx-Ax)t
(Ay-Cy)_(Dx-Cx) - (Dy-Cy)_(Ax-Cx) + (By-Ay)_(Dx-Ct =(Dy-Cy)_(Bx-Ax)t
(Ay-Cy)_(Dx-Cx) - (Dy-Cy)_(Ax-Cx) =(Dy-Cy)_(Bx-Ax)t(By-Ay)_(Dx-Cx)t
(Ay-Cy)_(Dx-Cx) - (Dy-Cy)_(Ax-Cx) =[(Dy-Cy)_(Bx-Ax)(By-Ay)*(Dx-Cx)]*t

[(Ay-Cy)*(Dx-Cx) - (Dy-Cy)*(Ax-Cx)] / [(Dy-Cy(Bx-Ax) -(By-Ay)*(Dx-Cx)] =t
