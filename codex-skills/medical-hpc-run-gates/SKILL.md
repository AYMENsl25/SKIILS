---
name: medical-hpc-run-gates
description: Prepare, launch, or audit medical imaging ML experiments on HPC with dataset provenance, scheduler checks, and completion evidence. Use for Slurm training or evaluation work, not ordinary local ML scripts.
---

# Medical HPC run gates

Establish the exact cohort, labels, split, code revision, environment, and intended comparison before changing or launching an experiment. Inspect current project files and scheduler state; treat earlier notes as leads rather than current facts.

Preserve source data, identifiers, credentials, checkpoints, and prior results. Keep protected data and generated outputs out of Git and shared reports unless explicitly authorized.

For a requested run, deliver executable code, configuration, and Slurm artifacts. Validate inputs and paths, run the smallest useful local or remote smoke check, then submit only when the current request authorizes it. Record job ID, code revision, command, data manifest, output path, and scheduler state. Verify that the job started and logs show meaningful progress.

Separate prepared, synthetic, smoke, running, completed, and evaluated evidence. A checkpoint or log line is not a completed result. Require finished scheduler status, expected outputs, held-out evaluation, and split accounting before interpreting model quality. State missing gates and the next concrete action.
