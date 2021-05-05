# Output documents

Two output documents will be taken into account to gauge the success of your algorithm.

## CSV

A CSV document with the following syntax must be produced by your algorithm:
```
Time (ms), X position (px), Y position (px)
```
One line per waypoints.

## Image

The output image must be the same size as the input satellite image. It must show the path taken by the hybrid drone as a continuous line.

The drawn lines shall be coloured in shades of red according to the speed of the vehicle at every point compared to its maximum possible speed (given in the provided problem constraints).  
Zero speed would thus be black (0, 0, 0) and maximum speed red (255, 0, 0).

