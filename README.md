# Single Cross Problem – Monte Carlo Simulation

## Problem Statement

A random line segment of length D is placed on an infinite 2D checkerboard grid with unit-length squares. We are interested in finding the value of D that **maximizes the probability** that the segment **crosses exactly one line**—either a vertical or a horizontal grid line, but **not both**.

---

## Simulation Approach

This notebook uses a **Monte Carlo simulation** to estimate the probability that a randomly placed and oriented segment of length D crosses **exactly one line**. We repeat this for various values of D to find the optimal length.

---

## Method Summary

1. **Random Segment Placement**  
   - A random point (i,k) is chosen within a unit square.  
   - A random angle theta determines the orientation of the line segment.  
   - The segment is centered at (x,y) and extends in the direction of 2pi.

2. **Intersection Check**  
   A helper function calculates how many grid lines (horizontal and vertical) the segment crosses using the floor of its endpoints' coordinates.

3. **Monte Carlo Estimation**  
   For each value of D, we run many iterations and count the proportion of segments that cross exactly one line.

4. **Optimization**  
   The simulation is run for a range of D values. The value of D with the **maximum estimated single-cross probability** is selected.

---

## Output

- The notebook outputs:
  - A graph of length Ds and their corresponding probabilities.
  - The estimated probability of of the optimal length D.

---

## Key Takeaways

- This is a geometric probability problem.
- Simulation gives insight where analytical calculation is challenging.
- The method leverages randomness to estimate probabilities, which is suitable due to the complexity of geometric intersections.
