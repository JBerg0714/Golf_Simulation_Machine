# Using an HD Golf Simulator to create an Autonomous Computational Model

The original purpose for this research was to reverse engineer an HD golf simulator through creating an autonomous computational model to show the trajectory of a golf ball while in flight. The idea was to take the output of data from an HD Golf simulator and use values such as: velocity, apex/peak, carry, launch angle and spin values to plug into physical equations to compare the computational trajectory of the golf ball to the trajectory of the golfball depicted on the screen of the simulator. We focused on shots with purely backspin to prevent having to analyze the data within 3-dimensions.

## Motivation

It is no secret that golf is a very complex sport. The ideology and rules of the game are as simple as they come; however, it is so difficult to efficiently execute accurate golf shots on a consistent basis. With this in mind, I thought that by understanding the physics of a golf shot that I would be able to drop a few strokes on my scorecard. 

## Coding Style 

All coding was completed in Jupyter Notebook (Jupyter - an acronym meaning Python). Below in the "Notebooks" section are links to each jupyter notebook used during the research. Within each jupyter notebook are notes to help walk you through what the code means. 

## Sources 
The following source was used to determine what equations to use for the lift force on the golf ball: [Source](https://github.com/JBerg0714/Golf_Simulation_Machine/blob/master/Source%20that%20was%20referenced.pdf)

## Using the HD Simulator 
The following are slow-motion clips of me taking a shot on the HD Simulator with a TaylorMade M2 pitching wedge.
- [Rear View](https://github.com/JBerg0714/Golf_Simulation_Machine/blob/master/Experimental%20Procedure%20Videos/1.mp4)
- [Side View](https://github.com/JBerg0714/Golf_Simulation_Machine/blob/master/Experimental%20Procedure%20Videos/2.mp4)
- [Trajectory](https://github.com/JBerg0714/Golf_Simulation_Machine/blob/master/Experimental%20Procedure%20Videos/3.mp4)
- [Rear View 2](https://github.com/JBerg0714/Golf_Simulation_Machine/blob/master/Experimental%20Procedure%20Videos/4.mp4)

## Notebooks
- [Trajectory Comparisons of Apex and Carry](https://github.com/JBerg0714/Golf_Simulation_Machine/blob/master/Jupyter%20Notebooks%20/golf-ball-rk4-v3.ipynb)
- [RMS Values](https://github.com/JBerg0714/Golf_Simulation_Machine/blob/master/Jupyter%20Notebooks%20/golf-ball-rk4-v4.ipynb)
- [Manual Derivation of Coefficients](https://github.com/JBerg0714/Golf_Simulation_Machine/blob/master/Jupyter%20Notebooks%20/golf-ball-rk4-v5.ipynb)
- [Testing Derived Coefficients](https://github.com/JBerg0714/Golf_Simulation_Machine/blob/master/Jupyter%20Notebooks%20/golf-ball-rk4-v6-(TESTDATA).ipynb)
- [RMS values with Derived Coefficients](https://github.com/JBerg0714/Golf_Simulation_Machine/blob/master/Jupyter%20Notebooks%20/golf-ball-rk4-v7-(TESTDATA).ipynb)
- [Optimization of Coefficients](https://github.com/JBerg0714/Golf_Simulation_Machine/blob/master/Jupyter%20Notebooks%20/golf-ball-rk4-v8-(TESTDATA).ipynb)
- [RMS values with Optimized Coefficients](https://github.com/JBerg0714/Golf_Simulation_Machine/blob/master/Jupyter%20Notebooks%20/golf-ball-rk4-v9.ipynb)
- [Percent Difference](https://github.com/JBerg0714/Golf_Simulation_Machine/blob/master/Jupyter%20Notebooks%20/golf-ball-rk4-v10.ipynb)
- [Presentation](https://github.com/JBerg0714/Golf_Simulation_Machine/blob/master/Presentation.ipynb)

## Credits
None of this would have been possible without the incredible mentoring of Dr. Aaron Titus of High Point University. Additionally, I would like to thank Dr. Eric Hegedus for providing us with access to the High Point University Biomechanics Lab as well as the HD Golf Simulator. 
