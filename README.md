# DiscoBox

A photonic quantum computer you can build at home, achieving cluster states equivalent to __8 qubits__ (and beyond!)

## The quick of it  

We aim our 405nm laser into our Spatial Light Modulator (a hologram) to physically carve the light into 16 unique modes we will use as dimensions (the OAM twist and the radials pictured in the next section).

It continues into our Beta Barium Borate(BBO) non-linear crystal to get our entanglement.

It continues into the second Spatial Light Modulator (SLM) where we bake the quantum gates directly into the phase (our "program" gets written here and "executed" at the detector). 

Finally it hits our Single Photon Avalanche Diode (SPAD) detector array, where we register our final output value (1-16) as a coincidence click. (our final output is a number 1-16)
![yes](images/simple_setup2.jpg)

None of this is original work I'm combining Forbes/He/Shen's dimension scaling and Lib&Bromberg's qudit partitioning, with the hopes that you can scale dimensions and thus effective qubit size relatively easy with better hardware. 

## Lets make some dimensions
![Alt text](images/oam-radial-modes.svg)

We're scaling our 405nm-laser-spdc-entagled-photons into high dimensions by twisting the orbital angular momentum (2 to the left and 2 to the right for **l=4** total) with our Spatial Light Modulators and altering the radials (**p=4**)  for 16 usable dimensions (**l*p**)  in preparation for the next step, <font size="2em">**hyper-dimensional-entaglement**</font> ( I'm calling it that - the creators [Lib & Bromberg](https://www.nature.com/articles/s41566-024-01524-w) called it "high-dimensional spatial encoding of cluster states")

## Hyper Dimensional Entaglement

Take our 16d Hilbert space we just created and partition it into "registers" where dimension=2 (a traditional qubit) which we connect via **tensor products** , which is the magic that gives us free gates (free on the same photon).
![no](images/single_photon_qudit_split.svg)

Cross photon gates get tricky, which also requires a bit of graph work upfront to split the circuit across photons so that interactions can occur for free.
![yes](images/two_photon_gate_structure.svg)

## The Next Step

Get a job to save up the money [to build this thing](BUILD.md)



## References

- He, C., Shen, Y. & Forbes, A. Towards higher-dimensional structured light. *Light Sci. Appl.* 11, 205 (2022). https://doi.org/10.1038/s41377-022-00897-3
- Lib, O. & Bromberg, Y. Resource-efficient photonic quantum computation with high-dimensional cluster states. *Nature Photonics* 18, 1218–1224 (2024). https://doi.org/10.1038/s41566-024-01524-w
