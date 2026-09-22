# DiscoBox

A photonic quantum computer you can build at home, targeting cluster states equivalent to __8 qubits__.

![Alt text](images/oam-radial-modes.svg)

## Lets make some dimensions

We're scaling our 405nm-laser-spdc-entagled-photons into high dimensions by twisting the orbital angular momentum (2 to the left and 2 to the right for **l=4** total) with our Spatial Light Modulators and altering the radials (**p=4**) with our q-plates (optics equipment) for 16 usable dimensions (**l*p**)  in preparation for the next step, <font size="2em">**hyper-dimensional-entaglement**</font> ( I'm calling it that - the creators [Lib & Bromberg](https://www.nature.com/articles/s41566-024-01524-w) called it "high-dimensional spatial encoding of cluster states")

## Hyper Dimensional Entaglement

Take our 16d Hilbert space we just created and partition it into "registers" where dimension=2 (a traditional qubit) which we connect via **tensor products** , which is what gives our free gates (free on the same photon).
![no](images/single_photon_qudit_split.svg)

Cross photon gates get tricky, which also requires a bit of graph work upfront to split the circuit across photons so that interactions can occur for free.
![yes](images/two_photon_gate_structure.svg)

## Putting it together

We aim our laser into our first SLM/Q-plate batch to physically carve the light into 16 modes we will use as dimensions. It then feeds into our BBO crystal to get our entagled photons. Then fed into the second SLM where we bake the gates directly into the phase. Finally it hits our SPAD detector array, where we register our final output value (1-16)

## References

- He, C., Shen, Y. & Forbes, A. Towards higher-dimensional structured light. *Light Sci. Appl.* 11, 205 (2022). https://doi.org/10.1038/s41377-022-00897-3
- Lib, O. & Bromberg, Y. Resource-efficient photonic quantum computation with high-dimensional cluster states. *Nature Photonics* 18, 1218–1224 (2024). https://doi.org/10.1038/s41566-024-01524-w
