December 27, 2019
Halo ice shelf
If player moves too fast, entire shelf breaks
If player moves to close to edges, edges breaks
Use trigger volumes for edges (proximity trigger)
Use a big volume for each shelf to check player velocity. If velocity reaches a low threshold, trigger cracking sound effects and particles
If velocity reaches a high threshold, shatter the shelf except for the part closest to the "wall"