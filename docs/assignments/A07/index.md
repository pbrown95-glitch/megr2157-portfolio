# A7 – [FEA on Bracket]

## Objective

-Use Finite Element Analysis (FEA) to improve the bracket design from previous assignments.
-Ensure high stiffness, strength, and lightweight optimization through iterative design.
-Conduct multiple FEA simulations, refining geometry based on results.
-Perform static stress analysis, including constraints, loading, and meshing selection.
-Interpret data by identifying max stress, displacement, and safety factors.
-Optimize the design by modifying geometry to enhance performance.
-Document the entire process with images, calculations, and insights.
-Reflect on key engineering lessons learned and time spent

## Description

The objective of this assignment is to improve the stiffness, strength, and weight of an existing bracket subjected to a 600 lbf strap load using finite element analysis in SolidWorks. Stress, displacement, and safety factor results will guide two successive geometry revisions while maintaining the assigned material. Before each revision, mesh refinement will be used to achieve a difference of 7% or less between successive analyses. If convergence is not achieved after three mesh attempts, the finest mesh results will be used to proceed with the design process.

## Design
The existing Aluminum 6061-T6 bracket was used as the baseline design, designated Design I. A slide connection supports the bracket and carries a 600 lbf strap load on its protruding rod. The original geometry was saved and documented before making any design modifications. The slide was constrained and fixed as it is the supporting component of the part. The load was applied to the rod where the strap goes. The material was also set to the material used during design. 
![w](design1.png)
![w](Design1_fixed.png)
![w](ForceApplied.png)
![w](Material.png)
These remain constant throughout all designs. 

 
### Design One
#### Iteration One 

For Design I’s initial mesh, a blended curvature-based mesh was selected with maximum and minimum element sizes of 0.4870in and 0.2669in, respectively. This coarse mesh will provide the initial results for comparison with subsequent mesh refinements.
![w](d1Mesh1.png)

The initial coarse-mesh analysis predicted a maximum von Mises stress of 651.2 MPa and a maximum resultant displacement of 11.08 mm. High stress occurred near the stem’s connection to the upper bracket, while maximum displacement occurred at the free end of the rod. The maximum stress exceeded the assigned material’s yield strength of 275 MPa, giving an estimated minimum safety factor of 0.422. Mesh refinement is required before using these results to guide geometry changes.
![w](d1strain1.png)
![w](d1Stress1.png)
![w](d1diss1.png)

#### Iteration Two
Starting off iteration two, the mesh was made finer. The maximum and minimum element size were set to 0.34in and 0.187in, respectively. In doing so, I hope to see little change in the reported safety factor, stress, strain, and displacement. Running the simulation returns the graphs as follows:
![w](Meshd12.png)
![w](Dissd12.png)
![w](Straind12.png)
![w](Stressd12.png)


#### Iteration Three
For iteration three, the mesh was made finer once again. This time, the maximum and minimum element sizes were set to 0.238in and 0.131in, respectively. With the element sizes set to a finer grain, the simulation was run, reporting these plots:
![w](Meshd13.png)
![w](Dissd13.png)
![w](Straind13.png)
![w](Stressd13.png)

#### Design One Report
Using the values found after running the FEA, the change from one mesh to another was tracked. These changes were quantified as a percent through the equation 100*(|Xf-Xo|/Xf), where Xf is the latest value, and Xo is the previous value. 
The desired convergence of 7% was not reached in every property through all three iterations, so I stopped at three. The inside corners of the stems that connect the rod to the slider undergo the most stress. The end of the rod furthest from the slider undergoes the most displacement. 
![w](d1.png)
![w](d11.png)


### Design 2


### Design 3

## Reflection
