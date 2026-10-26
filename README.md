# HalfLifeWeek2-CAD
**Merbl Guide:** https://github.com/karnxx/merbl/blob/main/guide.md

**My project:** https://cad.onshape.com/documents/eef34ff6aac3df2e3823ebc7/w/965d602a61f020e2ae6cffc8/e/b4a4600d7486f63eae61b30a?renderMode=0&uiState=6adfd530e5fd04602f649683

I designed a 3D-printed marble race course in Onshape following the Hack Club Half Life Week 2 guide. The guide was super helpful for learning the core Onshape tools, and I used it to build a complete course from scratch.

To add my own twist and go beyond a single basic path, I designed two separate tracks that run in opposite directions and merge at the end. I also wanted to include every custom obstacle from the guide, so my course features a funnel, a staircase, a plinko board, and a catch box at the bottom.

**Here is the final result:**
![Final result](./Pictures/Final%20Result.png)
![Final result 2](./Pictures/Final%20Result%202.png)

**How the course works:**
- **Track 1:** Curves around one side of the base and drops the marble into a funnel, where it spirals down and exits onto the plinko board.
![Track 1](./Pictures/Track%201.png)

- **Track 2:** Loops around the opposite direction, drops onto the staircase, and winds back around to feed into the same plinko board.
![Track 2](./Pictures/Track%202.png)

- **Finish:** Both paths meet at the plinko board, where the marble bounces through the pegs and lands in a catch box at the end.

**Why and how I made it:**
I made this project to get comfortable with 3D CAD modeling in Onshape. Instead of just making one simple track, I wanted to test out all the different modeling techniques covered in the guide and see how they could fit together into a single course.

I built the project in Onshape using these steps:
1. For the base, I sketched and extruded a flat baseplate on the Top Plane so the slicer's tree supports have a solid foundation to grow from and hold up the floating tracks.
2. For the standard tracks, I created slanted planes using Line Angle so the marble moves with gravity, sketched paths using lines, circles, and fillets (keeping curve radii above 12mm so the track wouldn't intersect itself), and used Composite Curve and Sweep with a 9mm inner / 14mm outer circular cut-out profile.
3. For the funnel, I sketched the cross-section profile with an angled wall and drop hole, used Offset for the 3mm wall thickness, and used Revolve around a central axis line.
4. For the staircase, I sketched the stepped profile, extruded the steps by 10mm (8mm marble diameter + 2mm clearance), and extruded 3mm side walls on both sides.
5. For the plinko board and catch box, I sketched a grid of 3x3mm aligned rectangles for the pegs, extruded the board and 16mm outer walls, chamfered the inside corners so the marble doesn't get stuck, and added a box at the bottom exit to catch the marble.
6. For the marble, I revolved a 4mm radius semicircle 360 degrees to create an 8mm sphere.
7. For the assembly, I used the Transform tool (Translate by XYZ) to position all the obstacles and tracks so the marble transitions smoothly from one section to the next.

I used the guide to help with a lot of these steps.

**3D printing instructions:**
1. Open [CAD Files/merbl-stl.stl](./CAD%20Files/merbl-stl.stl) in your 3D printer slicer.
2. Place the base flat on the build plate.
3. To enable supports, turn on Tree Supports (Tree Thin works best).
4. Check the support placement. To do this, preview the sliced layers to make sure supports only touch the outside of the tracks and obstacles. Make sure no supports are generated inside the track channels, funnel, or plinko pegs where they could block the marble.
5. Print the course and the 8mm marble using standard PLA (0.2mm layer height, 15% infill).
6. Test: Once the print finishes, leave the main tree supports attached to the baseplate to keep the tracks mounted, clear away any stray stringing inside the paths, and drop the marble at the top of either track to race!

**BOM:**

| Item | Qty | Supplier | Cost/item | Total Cost | Link |
|---|---:|---|---:|---:|---|
| 3D printing | 1 | Printing Legion | $18.00 | $18.00 | [Printing Legion](https://hackclub.slack.com/archives/C083P4FJM46/p1792359524697869) |
| Total |  |  |  | $18.00 |  |
