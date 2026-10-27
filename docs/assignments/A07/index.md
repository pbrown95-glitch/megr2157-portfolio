# A7 – FEA on Bracket

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
The desired convergence of 7% was not reached in every property through all three iterations, so I stopped at three. The inside corners of the stems that connect the rod to the slider undergo the most stress. The end of the rod furthest from the slider undergoes the most displacement. The mass of the unchanged design remains 1.85 lbs, the Minimum SF was 0.3317, the Number of Elements was 11,779, the maximum displacement was 11.73mm, and the Max stress was 829.1Mpa. 
![w](d1.png)
![w](d11.png)


### Design Two

Design one showed high stress near the junction between the stem and the upper bracket. To address this region, I added two 0.125 in radius fillets at the inside corners of the junction. These fillets added material locally and created a smoother transition between the stem and upper bracket. The stem thickness remained 0.25 in.
![w](Filletd2.png)

The Aluminum 6061-T6 material, fixed mounting faces, and 600 lbf downward load remained unchanged so the effects of the geometry revision could be evaluated.

#### Iteration One
For the initial Design II analysis, I used a mesh with maximum and minimum element sizes of 0.48702 in and 0.26686 in, respectively. This mesh contained 1,640 elements and 3,049 nodes.
![w](Meshd21.png)

The coarse-mesh analysis predicted a maximum von Mises stress of 860.8 MPa, a maximum resultant displacement of 11.11 mm, and a calculated minimum safety factor of approximately 0.3195. High stress remained near the stem-to-upper-bracket junction, while maximum displacement occurred at the free end of the rod again. The predicted stress exceeded the material’s yield strength of 275 MPa.
![w](Dissd21.png)
![w](Straind21.png)
![w](Stressd21.png)

#### Iteration Two
For the second iteration, I reduced the maximum element size to 0.340 in and the minimum element size to 0.187 in. This refinement increased the mesh to 4,363 elements and 7,420 nodes. The geometry, material, fixtures, and applied load remained unchanged. 
![w](Meshd22.png)

The refined analysis predicted a maximum von Mises stress of 842.1 MPa and a maximum resultant displacement of 10.41 mm. The minimum safety factor calculated from the rounded stress value was approximately 0.3266; the safety-factor plot reported a minimum of 0.3265. The stress distribution continued to show high stress near the filleted stem junction. Maximum displacement remained at the free end of the rod. 
![w](Dissd22.png)
![w](Straind22.png)
![w](Stressd22.png)

#### Design Two Report
Using the same formula as in design report one, all three properties were found to be within the assignment’s 7% convergence criterion. Therefore, I retained the second mesh and proceeded without a third mesh iteration. The number of elements was 4,363, the minimum SF was 0.3265, the Mass remained 1.85lb, the Max displacment was 10.41mm, and the Max stress was 842.1MPa. 
![w](d2.png)
![w](d22.png)

The fillets alone did not provide enough reinforcement to meet the safety-factor target of 4. The reported displacement decreased compared with Design 1, but the retained maximum stress did not improve. This stress comparison is limited because Design 1 did not achieve mesh convergence and the two designs used different retained mesh sizes.

### Design Three
Design 2 showed that adding root fillets alone did not provide enough reinforcement to meet the safety-factor target. For Design 3, I increased the stem thickness from 0.25 in to 1.00 in while retaining the two 0.125 in radius fillets. This change added material to the stem to increase its resistance to bending. The Aluminum 6061-T6 material, fixed mounting faces, and 600 lbf downward load remained unchanged.
![w](Extrusiond3.png)

#### Iteration One
For the initial Design III analysis, I used a mesh with maximum and minimum element sizes of 0.48702 in and 0.26686 in, respectively. This mesh contained 1,684 elements and 3,070 nodes.
![w](Meshd31.png)

The coarse-mesh analysis predicted a maximum von Mises stress of 124.9 MPa, a maximum resultant displacement of 0.7503 mm, and a calculated minimum safety factor of approximately 2.2018. The stress distribution showed high stress in the upper crosspiece near the stem junction. Maximum displacement occurred at the free end of the rod. Although the predicted stress was below the material’s yield strength of 275 MPa, mesh refinement was required before accepting these results.
![w](Dissd31.png)
![w](Straind31.png)
![w](Stressd31.png)

#### Iteration Two
For the second iteration, I reduced the maximum element size to 0.340 in and the minimum element size to 0.187 in. The refined mesh contained 4,675 elements and 7,802 nodes.
![w](Meshd32.png)

The analysis predicted a maximum von Mises stress of 166.1 MPa, a maximum resultant displacement of 0.7981 mm, and a calculated minimum safety factor of approximately 1.6556. Compared with the first mesh, maximum stress changed by 24.80%, maximum displacement changed by 5.99%, and minimum safety factor changed by 32.99%. Displacement met the 7% criterion, but stress and safety factor did not. Therefore, a third mesh iteration was required.
![w](Dissd32.png)
![w](Straind32.png)
![w](Stressd32.png)

#### Iteration Three
For the third iteration, I reduced the maximum element size to 0.238 in and the minimum element size to 0.131 in. This mesh contained 12,453 elements and 19,667 nodes.
![w](Meshd33.png)

The analysis predicted a maximum von Mises stress of 177.1 MPa and a maximum resultant displacement of 0.8294 mm. The calculated minimum safety factor was approximately 1.5528, consistent with the plotted minimum of 1.553. The maximum-stress annotation identified the underside of the upper crosspiece, just left of the stem junction, as the critical location. Maximum displacement remained at the free end of the rod.
![w](Dissd33.png)
![w](Straind33.png)
![w](Stressd33.png)

#### Design Three Report
Using the same calculation to find the change in the properties of interest, I found that from mesh 2 to 3, all were within 7%. The number of elements was 12,453, the minimum SF was 1.553, the mass changed this time to 1.97lb, the Max displacment was 0.8294mm, and the Max stress was 177.1MPa. 
![w](d3.png)
![w](d33.png)

Compared with Design 2’s retained results, Design 3 reduced maximum stress by approximately 79.0% and maximum displacement by approximately 92.0%. Mass increased from 1.85 lb to 1.97 lb, an increase of approximately 6.5% based on the rounded values. Increasing the stem thickness substantially improved the predicted response with a relatively small increase in total bracket mass. While still not reaching ideal values, the changes made a significant improvement to the structural stability of this part. 


## Reflection and Part Download

This assignment taught me to check mesh convergence separately from design performance. In Design 1, maximum stress increased from 651.2 MPa to 829.1 MPa as the mesh became finer, while displacement changed much less. This showed why stress, displacement, and safety factor each need a convergence check.

I initially confused meeting the 7% convergence criterion with reaching the safety-factor target of 4. Design 3 met the convergence criterion, but its minimum safety factor was only 1.553. I also learned that inside fillets add material, reinforcing sharp connections.

Increasing the stem thickness had a larger effect than adding fillets alone. Compared with Design 2, Design 3 reduced maximum stress by approximately 79% and displacement by 92%, while increasing mass by approximately 6.5%. Further improvement would focus on the upper crosspiece near the stem junction, where the final maximum stress occurred.

Total time spent: 4 hours, including modeling, simulation, calculations, and documentation.
[Download the SolidWorks Part](A7_1.SLDPRT)

