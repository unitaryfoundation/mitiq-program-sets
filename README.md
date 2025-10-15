# Program Sets Demo

This repository shows how to combine [Amazon Braket Program Sets](https://docs.aws.amazon.com/braket/latest/developerguide/braket-program-sets.html) with [Mitiq](https://mitiq.readthedocs.io/) zero-noise extrapolation (ZNE). The example builds a small two-qubit circuit, creates noise-scaled versions with Mitiq, and evaluates them as a batch through a `ProgramSet`.

## Getting Started

1. Download `uv`
2. Install dependencies:

   ```bash
   uv sync
   ```

3. Open the notebook `program-sets.ipynb` for the walkthrough.

## Next Steps

- Swap the `LocalSimulator` with a different Braket device (managed simulator or hardware) once you have the necessary AWS credentials configured.
- Experiment with other error mitigation techniques provided by Mitiq (for example, Clifford data regression or probabilistic error cancellation).
- Extend the `ProgramSet` with additional observables or jobs to build larger calibration and benchmarking workflows.
