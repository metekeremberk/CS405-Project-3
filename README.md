# Solar System Simulation Project Report

This report details the implementation of three tasks for the solar system simulation project, focusing on scene graph implementation, illumination, and scene expansion.

## Task 1: Scene Graph Implementation

In `sceneNode.js`, the `draw` method was implemented to handle transformation propagation through the scene graph. The key modifications include:

- Implemented matrix transformations that propagate from parent to child nodes
- Applied transformations to MVP (Model-View-Projection), ModelView, Normal, and Model matrices
- Used the TRS (Translation-Rotation-Scale) transformation matrix for each node
- Implemented recursive drawing of child nodes with transformed matrices
- Ensured proper mesh drawing when a MeshDrawer is present

## Task 2: Illumination Implementation

In `meshDrawer.js`, the fragment shader was enhanced to implement diffuse and specular lighting. The modifications include:

- Added diffuse lighting calculation using the dot product of normal and light direction vectors
- Implemented specular lighting using the Phong reflection model
- Used a Phong exponent of 8.0 for specular highlights
- Maintained existing ambient lighting component (0.35)
- Applied lighting calculations only to non-light source objects
- Combined ambient, diffuse, and specular components with texture sampling

## Task 3: Mars Addition

In `project3.html`, Mars was added to the solar system as a child of the Sun node. The implementation included:

- Created a new MeshDrawer instance for Mars
- Set up Mars's texture using the provided Mars texture URL
- Configured Mars's position (-6 units on X-axis) relative to the Sun
- Set Mars's scale to 0.35 uniformly
- Implemented Mars's rotation to be 1.5 times the Sun's rotation speed
- Added Mars as a child node of the Sun in the scene graph

## Conclusion

In this project, we built a simple solar system animation that shows the Sun, Earth, Moon, and Mars. We made sure that the planets move correctly in relation to each other, added proper lighting to make them look more realistic, and successfully added Mars to the scene. All three tasks were completed as required, resulting in a working solar system model that clearly shows the movement and appearance of the celestial bodies.
