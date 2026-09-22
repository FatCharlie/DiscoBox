# DiscoBox

A photonic quantum computer you can build at home, targeting cluster states equivalent to __8 qubits__ (and beyond!)
Status: design phase, not yet built.

## The quick of it  

We aim our 405nm laser into our Spatial Light Modulator (a hologram) to physically carve the light into 16 unique modes we will use as dimensions (the OAM twist and the radials pictured in the next section).

It continues into our Beta Barium Borate (BBO) non-linear crystal where occasionally one 405nm photon splits into two 810nm daughter photons and become entangled via Spontaneous Parametric Down Conversion (SPDC). Seeding the crystal with a pump beam that's already in superposition across our 16 modes (**l&p**) gives us our full 16-dimensional state space per photon.

It continues into the second Spatial Light Modulator (SLM) where we bake the quantum gates directly into the phase (our "program" gets written here and "executed" at the detector). 

Finally it hits our Single Photon Avalanche Diode (SPAD) detector array, where we register our final output (an agreeing pair of numbers between 1-16, one per entagled photon).

![yes](images/simple_setup2.jpg)  

None of this is original work I'm combining Forbes/He/Shen's dimension scaling and Lib&Bromberg's qudit partitioning, with the hopes that you can scale dimensions and thus effective qubit size relatively easy with better hardware. 

## Let's make us some dimensions
![Alt text](images/oam-radial-modes.svg)

We're scaling our 405nm-laser-spdc-entangled-photons into high dimensions (by dimensions here I mean degrees of freedom) by twisting the orbital angular momentum (2 to the left and 2 to the right for **l=4 distinct values {-2,-1,1,2}**) with our Spatial Light Modulators and altering the radials (**p=4 distinct values {0,1,2,3}**)  for 16 usable dimensions (**l*p**)  in preparation for the next step, which I normally say with jazz hands: ***hyper-dimensional-entanglement*** (the creators [Lib & Bromberg](https://www.nature.com/articles/s41566-024-01524-w) call it "high-dimensional spatial encoding of cluster states")

## Hyper Dimensional Entanglement

Take our 16d Hilbert space we just created and partition it into "registers" where dimension=2 (a traditional qubit) which we connect via **tensor products** , which is the magic that gives us free gates (free on the same photon).
![no](images/single_photon_qudit_split.svg)

Cross photon gates get tricky, which also requires a bit of graph work upfront to split the circuit across photons so that interactions can occur for free.
![yes](images/two_photon_gate_structure.svg)

But this gives you 4 usable qubits per photon. If you want to build a full GHZ state from registers 1,2&3 via a H and two CNOT's you can totally do that. 

## The Next Step

[Build it!](BUILD.md). Confirm the Bell experiments, you can't trust it unless you replicate it yourself.

References
He, C., Shen, Y. & Forbes, A. Towards higher-dimensional structured light. Light Sci. Appl. 11, 205 (2022). https://doi.org/10.1038/s41377-022-00897-3
Lib, O. & Bromberg, Y. Resource-efficient photonic quantum computation with high-dimensional cluster states. Nature Photonics 18, 1218–1224 (2024). https://www.nature.com/articles/s41566-024-01524-w
