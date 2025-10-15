# Program Sets Demo

This repository shows how to combine [Amazon Braket Program Sets](https://docs.aws.amazon.com/braket/latest/developerguide/braket-program-sets.html) with [Mitiq](https://mitiq.readthedocs.io/) zero-noise extrapolation (ZNE). The example builds a small two-qubit circuit, creates noise-scaled versions with Mitiq, and evaluates them as a batch through a `ProgramSet`.

## Getting Started

1. Create and activate a virtual environment.
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

   or with Poetry:

   ```bash
   poetry install
   ```

3. Run the example script to execute the workflow from the command line:

   ```bash
   python examples/run_program_set_demo.py
   ```

4. Open the notebook for a guided walkthrough:

   ```bash
   jupyter notebook program-sets.ipynb
   ```

## Project Layout

- `src/program_sets_demo/`: Reusable utilities that build the circuit, construct the `ProgramSet`, and aggregate mitigated results.
- `examples/run_program_set_demo.py`: Minimal CLI entry point that prints raw and mitigated expectation values.
- `program-sets.ipynb`: Notebook version of the demo with additional explanation and output inspection.

## Requirements

- Python 3.9+
- [amazon-braket-sdk](https://github.com/aws/amazon-braket-sdk-python)
- [mitiq](https://github.com/unitaryfund/mitiq)
- [jupyter](https://jupyter.org/)

## Next Steps

- Swap the `LocalSimulator` with a different Braket device (managed simulator or hardware) once you have the necessary AWS credentials configured.
- Experiment with other error mitigation techniques provided by Mitiq (for example, Clifford data regression or probabilistic error cancellation).
- Extend the `ProgramSet` with additional observables or jobs to build larger calibration and benchmarking workflows.
