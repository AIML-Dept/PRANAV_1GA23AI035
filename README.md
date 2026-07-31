# Quantum Computing: Weekly Assignments

**Pranav Pujari** | USN 1GA23AI035 | Dept. of AI & ML

Weekly quantum computing lab assignments written in [Qiskit](https://www.qiskit.org/),
run on the Aer simulator. Each week has five notebooks, ordered by difficulty:
`EASY`, `MEDIUM`, `HARD`, `CHALLENGE`, `REALWORLD`.

---

## Week 1: Circuits and Measurement

Building circuits, running them, and looking at the measurement results.

| Notebook | What it does |
|---|---|
| `EASY` | Checks the setup. Prints the Qiskit version and the available Aer simulation methods. |
| `MEDIUM` | Puts one qubit into superposition with a Hadamard gate. Measured over 1024 shots and plotted as a histogram. Result is roughly 50/50. |
| `HARD` | Same idea with 3 qubits. All 8 outcomes should show up about equally, close to 1/8 each. |
| `CHALLENGE` | Runs the 3-qubit circuit twice: once on a perfect simulator, once with the `FakeManilaV2` noise model. Shows how noise skews the results. |
| `REALWORLD` | Uses 8 qubits as a random number generator and compares it to Python's `random.randint` over 1000 samples. |

## Week 2: Statevectors and the Bloch Sphere

Looking at the qubit state itself instead of measurement counts, and plotting it
on the Bloch sphere.

| Notebook | What it does |
|---|---|
| `EASY` | Applies an X gate (quantum NOT) to one qubit and prints the statevector. |
| `MEDIUM` | Chains two gates, Hadamard then Phase (S), and plots where the qubit ends up on the Bloch sphere. |
| `HARD` | Moves to 2 qubits. Hadamard on both gives an equal mix of all four states. |
| `CHALLENGE` | Builds any state you want from two rotation angles, theta and phi, then plots it. |
| `REALWORLD` | Compares a clean \|+> state against the same state after random phase noise. |

---

## Running the notebooks

```bash
pip install qiskit qiskit-aer qiskit-ibm-runtime matplotlib numpy pylatexenc
jupyter notebook
```

`pylatexenc` is needed for the `qc.draw('mpl')` circuit diagrams to render.
