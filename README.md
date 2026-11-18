# 🐱 Purr-fectly Protected Qubits: the interactive cat notebook

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/keremyurtseven/learn_cats/blob/main/cat_qubits_interactive.ipynb)

Companion notebook to the science-slam talk **"Purr-fectly Protected Qubits"** at **PushQuantum 2026** (Munich, 20 November 2026) by Kerem Yurtseven (TU Delft).

The notebook follows the talk slide by slide with short [QuTiP](https://qutip.org) simulations. It covers why a transmon is a qubit, why a cat qubit only suffers phase flips, how to make, stabilize and control a cat, and how to entangle two cats with a bias-preserving CX gate. Cells marked 🎛️ have sliders and play buttons: grow a cat, watch gates run frame by frame, and lose a photon at the worst possible moment.

## What's inside

| # | Section | Interactive 🎛️ |
|---|---|---|
| 1 | The Transmon | |
| 2 | What does a lost photon do? | |
| 3 | Initializing the Cat | grow the cat; the vacuum-to-cat ramp |
| 4 | QEC with Cats | qubits per logical qubit: surface code vs repetition code |
| 5 | Cat Qubit Stabilization | shrinking vs Kerr vs dissipative cats |
| 6 | Cat Qubit Control | Z gate; X gate with an optional lost photon |
| 7 | Bias-Preserving X | rotating the walls, with an optional lost photon |
| 8 | Bias-Preserving CX | the CX gate for control states 0, 1 and + |
| 9 | Bonus: a lossy CX on a GPU with jaxquantum | |

## Run it

**In your browser, no install needed:** click *Open in Colab* above, then *Runtime → Run all*.
The first cell installs QuTiP.

**On your computer:**

```bash
pip install qutip numpy scipy matplotlib ipywidgets jupyter
jupyter notebook cat_qubits_interactive.ipynb
```

or with conda:

```bash
conda create -n cats -c conda-forge python=3.11 qutip matplotlib ipywidgets jupyter
conda activate cats
jupyter notebook cat_qubits_interactive.ipynb
```

## The research behind it

Section 8 simulates the effective CX Hamiltonian of Puri *et al.* (2020). The preprint below shows how to build that gate with a single asymmetrically threaded SQUID (ATS) coupler: a 50 ns CX with 99.69% fidelity without photon loss, which keeps the cats' noise bias.

> K. Yurtseven *et al.*, *Bias-Preserving Entanglement of Kerr-Cat Qubits with an ATS Coupler*,
> [arXiv:2610.28749](https://arxiv.org/abs/2610.28749) (2026).

## Key references

* P. T. Cochrane, G. J. Milburn & W. J. Munro, [PRA 59, 2631 (1999)](https://doi.org/10.1103/PhysRevA.59.2631)
* M. Mirrahimi *et al.*, [NJP 16, 045014 (2014)](https://doi.org/10.1088/1367-2630/16/4/045014)
* S. Puri, S. Boutin & A. Blais, [npj Quantum Inf. 3, 18 (2017)](https://doi.org/10.1038/s41534-017-0019-1)
* J. Guillaud & M. Mirrahimi, [PRX 9, 041053 (2019)](https://doi.org/10.1103/PhysRevX.9.041053)
* A. Grimm *et al.*, [Nature 584, 205 (2020)](https://doi.org/10.1038/s41586-020-2587-z)
* S. Puri *et al.*, [Sci. Adv. 6, eaay5901 (2020)](https://doi.org/10.1126/sciadv.aay5901)

The full list is at the end of the notebook.

## License

Released under the MIT License. See [LICENSE](LICENSE).

## Contact

Questions or comments: keremyurtseven@tudelft.nl

*Claude Opus 5.5 was used as an assistant in preparing this notebook.*
