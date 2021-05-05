# Efficient scanning of a lake

You are provided with an aerial map of a body of water.
Your goal is to determine the boundary of the water surface in order to be able to plan a path that an aquatic drone will have to take to scan the depth of this lake.

## Water surface detection

Any technique could be used to identify and map the water surface. Use your imagination! Beware though that the results of this step will determine the success of the path planning algorithm. A ground truth map will be provided for the training data sets but not for the real one.

## Path planning

Now that you have a good representation of the water surface, you must determine the best path to scan it at a minimum resolution of **16** meters (every point of the water surface must be no further than 8 meters from the chosen path).

The fastest scan of the whole lake is the best one. To determine the speed of the scan, the following parameters are provided:

- Maximum speed: 5 m/s
- Acceleration: 1 m/s²
- Deceleration: 0.5 m/s²
- Maximum speed at waypoint: `1.2 (cos(Θ) + 1)² + 0.2` m/s with Θ taken as the angle between the incoming vector and outgoing vector of the waypoint in radians.
- Speed limit near the edge: `0.25 D + 0.5` m/s with D taken as the distance to the edge of the water.

The start and stop points of the generated path shall be the same point. It shall be on the edge of the water surface.

## Output

See the Output.md document for output formating.
