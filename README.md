# Platelet Glycoprotein Clustering Model Validation

This repository contains two complementary approaches for modelling platelet
glycoprotein receptor clustering:

- an agent-based model implemented in NetLogo; and
- a deterministic and stochastic ordinary differential equation (ODE) model
  implemented in MATLAB.

The models investigate how ligand valency and diffusion, receptor dimerisation,
cross-linking, phosphorylation, and spatial cluster structure affect receptor
clustering and dephosphorylation. Both approaches provide graphical outputs;
the NetLogo model can also export data from individual runs or BehaviourSpace
experiments as tables or CSV files.

## Repository contents

- [`Agent Based Modelling/`](./Agent%20Based%20Modelling/) - NetLogo agent-based
  models.
- [`ABM Extension Model.nlogox`](./ABM%20Extension%20Model.nlogox) - NetLogo
  6 model archive.
- [`ODE Modelling/MATLAB/`](./ODE%20Modelling/MATLAB/) - MATLAB scripts for
  deterministic ODE, steady-state, stoichiometric, and stochastic analyses.
- [`ODE Modelling/MATLAB/Models/`](./ODE%20Modelling/MATLAB/Models/) - model
  definitions, including a template and example Model 1.
- [`MATLAB_README.md`](./MATLAB_README.md) - detailed MATLAB setup and usage
  instructions.
- [`User Manual for ODE Models in MATLAB.pdf`](./User%20Manual%20for%20ODE%20Models%20in%20MATLAB.pdf) -
  user manual for the MATLAB model framework.
- [`LICENSE.md`](./LICENSE.md) - GPL-3.0-or-later licence text.

## Requirements

### NetLogo

- NetLogo 6.1 or later
- The NetLogo model may be opened as a `.nlogo` file or as a `.nlogox` archive

### MATLAB

- MATLAB R2019a or later
- MATLAB optimisation, plotting, and symbolics functionality used by the
  accompanying scripts

## Quick start

### Agent-based model

1. Open NetLogo.
2. Open [`Agent Based Modelling/ABM v9.nlogo`](./Agent%20Based%20Modelling/ABM%20v9.nlogo),
   or open [`ABM Extension Model.nlogox`](./ABM%20Extension%20Model.nlogox).
3. Press **Setup** to initialise the simulation, then press **Go** to run it.
4. Adjust the model controls to change ligand, receptor, phosphorylation,
   dimerisation, and clustering parameters.

### MATLAB ODE model

1. Add the MATLAB source directory to the MATLAB path:

   ```matlab
   addpath(genpath(fullfile(pwd, "ODE Modelling", "MATLAB")));
   ```

2. Run the example model:

   ```matlab
   Models(1)
   ```

3. Plot a time course or generate an analysis. For example:

   ```matlab
   Plot(1, 1:3)
   Plot(1, 1:3, "Proportion")
   Plot(1, 1:3, "T", 100)
   ```

See [`MATLAB_README.md`](./MATLAB_README.md) for model creation, plotting,
stoichiometric analysis, steady-state analysis, and stochastic simulation
instructions.

## Validation and publication

The repository is intended to support comparison between spatial,
agent-based behaviour and deterministic or stochastic kinetic descriptions.
No fixed validation thresholds or benchmark datasets are included in this
README; use the model documentation and publication-specific parameters
described in the associated study when reproducing published results.

## Citation

Please cite the associated publication. Citation details are not yet included
in this repository.

## Licence

This project is distributed under the terms of the GNU General Public Licence
v3.0 or later. See [`LICENSE.md`](./LICENSE.md).
