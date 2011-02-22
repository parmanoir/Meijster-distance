Meijster distance
==
[A General Algorithm for Computing Distance Transforms in Linear Time](http://dissertations.ub.rug.nl/FILES/faculties/science/2004/a.meijster/c2.pdf)
The Meijster distance computes a distance field from a boolean image. A boolean image is made up of zeros and ones, where zero means background (empty space) and one foreground. The resulting distance field is an image whose pixels store distance to foreground.

A distance field can be used for stroking shapes, computing [Voronoi diagrams](http://en.wikipedia.org/wiki/Voronoi_diagram), pathfinding, or performing [mathematical morphology](http://en.wikipedia.org/wiki/Mathematical_morphology) operators. The distance field changes depending on the distance function used. Each distance function uses a different shape to compute distance, hold down option ⌥ to reveal it. 

[Euclidean distance](http://en.wikipedia.org/wiki/Euclidean_distance)
-
This is the most commonly used distance function. Given a distance field (x,y) and an image (i,j) the distance field stores the euclidean distance : <code>sqrt((x-i)2+(y-j)2)</code>

Pick a point on the distance field, draw a circle using that point as center and the distance field value as radius. The circle will hit the closest foreground point. 

[Manhattan distance](http://en.wikipedia.org/wiki/Manhattan_distance) (Taxicab geometry)
-
The distance field stores the Manhattan distance : <code>abs(x-i)+abs(y-j)</code>

Pick a point on the distance field, draw a diamond (rhombus) using that point as center and the distance field value as radius. The diamond will hit the closest foreground point. 

[Chessboard distance](http://en.wikipedia.org/wiki/Chessboard_distance) (Chebyshev)
-
The distance field stores the chessboard distance : <code>max(abs(x-i),abs(y-j))</code>

Pick a point on the distance field, draw a square using that point as center and the double distance field value as edge length. The square will hit the closest foreground point.
