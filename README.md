# DIAMOND – IAM Model Diagnostics

## Overview

Python-based notebook for calculating diagnostic indicators from Integrated Assessment Model (IAM) scenario results, developed within the Horizon Europe DIAMOND project.

The methodology follows Harmsen et al. (2021), as adapted in DIAMOND Deliverable D6.7, *Open Science Protocols & Diagnostics*.

The diagnostics aim to characterise and compare IAM responses to climate mitigation policies, complementing automated validation and historical vetting.

## Diagnostic Indicators

| Indicator | Description |
|---|---|
| Relative Abatement Index (RAI) | Relative CO₂ emissions reduction between baseline and policy scenarios. |
| Emission Reduction Type (ERT) | Relative contributions of carbon-intensity and energy-intensity reductions. |
| Transformation Index (TI) | Changes in primary energy composition relative to the base year. |
| Fossil Fuel Reduction (FFR) | Reduction in fossil primary energy consumption relative to the base year. |
| Inertia Timescale (IT) | Persistence of emissions differences following delayed policy implementation. |
| Cost per Abatement Value (CAV) | Relationship between mitigation costs, emissions reductions, and carbon prices. |

## Input Data

The routines use model results in the IAMC reporting format, containing five index columns:

`Model`, `Scenario`, `Region`, `Variable`, `Unit`

Additional columns contain model results for individual years.

The computational workflow involves selecting the required IAMC variables, restructuring the input data, and aligning scenarios and years before calculating the indicators.

RAI, ERT, and CAV require baseline and policy scenario comparisons. TI and FFR can be calculated from individual scenario trajectories, while the original IT formulation requires a dedicated delayed-policy experiment.

Indicator availability depends on the variables and scenario configurations provided by each model.

## Methodological Considerations

Diagnostic results depend on scenario assumptions, variable definitions, and temporal coverage. Meaningful comparisons across models generally require harmonised scenario configurations.

The indicators characterise model behaviour rather than establish pass/fail criteria.

The Python routines provide the computational basis for the planned integration of diagnostics into the DIAMOND online validation tool.

## References

Harmsen, M., et al. (2021). Integrated assessment model diagnostics: Key indicators and model evolution. *Environmental Research Letters, 16*(5), 054046. https://doi.org/10.1088/1748-9326/abf964

DIAMOND (2025). *D6.7 – Open Science Protocols & Diagnostics*. Horizon Europe DIAMOND Project.

## Acknowledgement

This work was developed within the DIAMOND project, funded by the European Union's Horizon Europe research and innovation programme under Grant Agreement No. 101081179.
