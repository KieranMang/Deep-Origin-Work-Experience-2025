This was work experience conducted at the company Deep Origin, a company which combines molecular physics with AI-driven acceleration to revolutionize in silico drug discovery.
Slideshow: https://docs.google.com/presentation/d/1SoCFP2fO2HPwATfYw2MJgYKsHie7LeceCzRuv1C5Ntc/edit?usp=sharing

# A cube of side length 3 nanometers filled with water
https://github.com/user-attachments/assets/ab2ca49f-60fd-4e62-bc63-b9c2842f193c

# A simulation of the water at 300K for 100 picoseconds
https://github.com/user-attachments/assets/36c9983f-0057-4190-93dc-8c7503983495
(The molecules are simulated in a periodic space where molecules can exit from one end and enter the other, pacman like.)

# Radial Distribution Function
## Model Graph
<figure>
  <img width="834" height="610" alt="Model Graph of RDF" src="https://github.com/user-attachments/assets/87959f4b-3a47-4777-9eb0-84de378974ec" />
  <figcaption>Density, structure, and dynamics of water: The effect of van der Waals interactions Available to Purchase Jue Wang; G. Román-Pérez; Jose M. Soler; Emilio Artacho; M.-V. Fernández-Serra</figcaption>
</figure>


The Radial Distribution Function (g(r)) describes how density varies compared to the distance from a reference particle.
It is basically the probability of finding the center of a molecule (the oxygen atom in this case) within the distance of r and r + Δr.


# The built in implementation with MDTraj
Uses the built in function in the MDTraj python library, we obtain the expected graph with the same shape and a peak at around 3 Å.
<img width="567" height="432" alt="Matplotlib Graph matching Model Graph" src="https://github.com/user-attachments/assets/6cfcaac4-05ed-4abc-8b5b-a3d5444fe07a" />

# Handmade implementation
<img width="567" height="432" alt="Matplotlib Graph matching Model Graph" src="https://github.com/user-attachments/assets/e55168c2-16a0-438a-81b4-5e6fa810dd1d" />
Again we see the correct shape and the peak in the same spot.

# O-H RDF (Distances measured between Oxygen and Hydrogen)
<img width="576" height="438" alt="31ed95d4-d819-4e55-9756-dfc7272b12a0" src="https://github.com/user-attachments/assets/c2bedab3-5104-4ee3-a124-b0c17613ae9d" />
<figure>
  <img width="1600" height="781" alt="1124dc88-3373-4276-b87b-2ed647d09b50" src="https://github.com/user-attachments/assets/55d7633b-672d-4889-bc78-de8a6d5943d5" />
  <figcaption>Model graph for O-O and O-H</figcaption>
</figure>
The first initial spike goes beyond 400 and is the point where the radius is longer than the bond length between O and H in water (0.9572 Å in TIP3P). The two other peaks are in roughly the same positions as the ideal graph.

# How simulation time affects g(r) graph for diff. temps
![216da838-fd40-40bf-8e84-85febc214d9e](https://github.com/user-attachments/assets/edc4bae9-9fd7-47be-80f0-1083a1e10029)
![e5a6ec93-00b2-44b7-a722-f660e793dcab](https://github.com/user-attachments/assets/f5b1c1a3-38c8-4600-816d-0e55b54fbc47)
![22f15ae6-a295-46ef-af92-09da0d1fb6c1](https://github.com/user-attachments/assets/f560021f-5a91-48e2-a179-22c4d7ebeb56)
![3842e1f7-51d7-4c8f-bd7d-05b2530b5ed7](https://github.com/user-attachments/assets/694270ee-87c5-4e47-b66b-8738f716a453)
![a1f56987-b8f9-4bef-b284-60433cb9d6cb](https://github.com/user-attachments/assets/7e711d85-f687-406d-bfb6-575ed3035066)

# A  5 nm cube with a caffeine molecule and Na+ and Cl- ions
<img width="630" height="535" alt="8a383fed-29d4-446a-81bd-645f9b01bc1d" src="https://github.com/user-attachments/assets/12a031c2-cdfd-4317-a06c-77bba2a326cb" />

# Caffeine displacement over 5 simulations
<img width="570" height="453" alt="7196a76f-db89-4003-aafd-1ac1d8e302ff" src="https://github.com/user-attachments/assets/50378fba-1fcc-4a3d-963f-7bac1f494e91" />

# Caffeine Displacement 162 simulations
<img width="567" height="453" alt="f1dd68dd-2b6a-4529-a3f1-10695c4e9b13" src="https://github.com/user-attachments/assets/535806b8-fef2-4936-94af-221e196f6747" />
You can see the formings of logarithmic and linear graphs in the two graphs on the right. (As to be expected)

# The average of the previous graph
<img width="576" height="438" alt="31ed95d4-d819-4e55-9756-dfc7272b12a0" src="https://github.com/user-attachments/assets/c2bedab3-5104-4ee3-a124-b0c17613ae9d" />
<figure>
  <img width="428" height="337" alt="24cf9d86-c29a-45ac-9df9-9b52e62cf870" src="https://github.com/user-attachments/assets/27a29f8a-a8b2-41c4-8daa-baf0eac62fce" />
  <figcaption>Model graph</figcaption>
</figure>
<img width="567" height="453" alt="ab1ac436-6ad3-41de-bd16-9ab227d7fb30" src="https://github.com/user-attachments/assets/e00e33e3-f446-4229-9d37-2d24898e7691" />

# Differentiation of previous graph
<img width="619" height="453" alt="bb7167de-5f9a-4a8c-9d6b-57c1f498f6b6" src="https://github.com/user-attachments/assets/1bcf0b7f-5d5b-4660-bb0f-bdf09a0864e5" />
In three dimensions the Mean Square Displacement is MDS=6Dt with D being the diffusion coefficient of the liquid. The number above correlating to a 5.7x10^-9 m^2/s. In reality this should be closer to 6.8x10^−10 m^2/s. This is quite a bit off but as you can see, we would probably need more simulations.

# Av. displacement squared of water molecules in 162 sims
<img width="583" height="453" alt="92fa4925-9c9d-4dbd-b353-790a1aeb7bab" src="https://github.com/user-attachments/assets/10648ada-6867-4185-842b-a8d940a33b02" />

# Prev. Graph averaged over every simulation
<img width="567" height="453" alt="cb6e5438-ff6d-4b89-a02a-0b45476e1c1a" src="https://github.com/user-attachments/assets/5328fe3e-f6ca-499f-a985-e4619d7529b0" />
<figure>
  <img width="428" height="337" alt="24cf9d86-c29a-45ac-9df9-9b52e62cf870" src="https://github.com/user-attachments/assets/27a29f8a-a8b2-41c4-8daa-baf0eac62fce" />
  <figcaption>Model graph again</figcaption>
</figure>
We see that the graph is remarkably similar to what is expected. The small curved part at the start of the graph is part of a parabola, this is when the initial velocities of the particles have not randomised and the particles haven’t hit any others yet, thus the displacement is proportional to time elapsed and displacement squared increases quadratically with time.

# Differentiation of previous graph
<img width="606" height="453" alt="190e4665-7847-43e3-b917-36fa12f57525" src="https://github.com/user-attachments/assets/6f64591c-f3eb-4e89-8b4f-56cd8210caef" />
<img width="338" height="119" alt="50ea870d-9db1-4d52-abcb-3abed60a6a68" src="https://github.com/user-attachments/assets/baa5b4e9-01e0-4db9-bc4c-384198995551" />
In three dimensions the Mean Square Displacement is MDS=6Dt with D being the diffusion coefficient of the liquid. The number above correlating to a 4.05×10−9 m^2/s. In reality this should be closer to 2.299x10^−9 m^2/s for pure water but this may have something to do with the TIP3P water model and the other particles in the water.
