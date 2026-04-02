# h-irace

**h-irace** is an extension of the iRACE framework that incorporates concurrent racing processes over predefined heterogeneous instance subsets.

## Overview

h-irace extends the irace framework to handle heterogeneous instance sets—collections of problem instances with different difficulties that can produce different results with different configurations. The framework implements concurrent independent irace procedures, with the budget equally split across instance subsets. This enables more effective configuration tuning when instances vary significantly in their characteristics.

## Branches

h-irace provides multiple implementation variants to support different tuning strategies:

### Main Implementation
**h-irace** - The core implementation that runs concurrent independent irace procedures, one for each heterogeneous instance subset with equally distributed budget.

### Convergence Detection Methods (AC)
These branches detect when an instance subset's tuning process has converged, enabling budget transfer between subsets:

- **h-irace-AC-1** - Convergence detection method 1
- **h-irace-AC-2** - Convergence detection method 2
- **h-irace-AC-3** - Convergence detection method 3

### Warm-up Phase with Convergence (WAC)
These branches implement an additional warm-up phase where initial tuning is performed using all instances regardless of subset assignment. This shared warm-up phase provides better starting points for the subsequent independent concurrent tuning processes on each instance subset:

- **h-irace-WAC-1** - Warm-up phase with convergence detection method 1
- **h-irace-WAC-2** - Warm-up phase with convergence detection method 2
- **h-irace-WAC-3** - Warm-up phase with convergence detection method 3

## Setup Instructions

[**User Guide (PDF)**](https://cran.r-project.org/package=irace/vignettes/irace-package.pdf) 

## Attribution

Based on **irace** - Copyright (C) 2010-2020 Manuel López-Ibáñez, Jérémie Dubois-Lacoste and Leslie Pérez-Cáceres.
