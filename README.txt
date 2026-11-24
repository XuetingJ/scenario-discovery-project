Australian domestic aviation: scenario inputs and 2050 lifecycle emissions

futures_2050.csv: 10,000 equal-weight Latin hypercube simulations (seed 123).
reference_pathways_2050.csv: nine separate reference pathways, not part of the
Latin hypercube sample. Low/Medium/High designations match Supplementary Table
S1. In reference identifiers, NZ denotes the High SAF setting, not net zero.

Data dictionary
- future_id: saved simulation row identifier.
- gA: continuously compounded annual activity growth, fraction per year.
- rEI: continuously compounded annual effective energy-intensity improvement,
  fraction per year. Positive values indicate falling energy intensity.
- rho: neat SAF lifecycle abatement relative to fossil jet fuel, as a fraction.
- s_max: ceiling on the delivered SAF share of aviation fuel by energy,
  as a fraction. The scenario reaches the ceiling in 2050.
- emissions_2050: 2050 lifecycle emissions in Mt CO2e, Australian financial
  year ending in 2050.
- vulnerable_q80, vulnerable_q90, vulnerable_q95: 1 if emissions exceed the
  corresponding limit, 0 otherwise. The reductions are relative to FY2018-19
  lifecycle emissions of 11.482335 Mt CO2e. The saved limits are 2.296467,
  1.1482335 and 0.574116750000001 Mt CO2e, respectively.
- inside_primary_lhs (reference pathways only): TRUE if the reference
  coordinates are within or on the boundary of the primary sampled domain.

Provenance and scope
Inputs, endpoint emissions and flags are selected at saved precision from
futures_2050.csv, overlay_coordinates.csv and overlay_exact_outcomes.csv of
the 4 September 2026 run. The nine reference inputs agree with Table S1 at the
displayed precision. The sampled exceedance counts are 8,217, 9,707 and 9,974.
Eight of nine reference pathways exceed the 90% benchmark.
These are simulations, not forecasts or observational data. Equal weights
describe the sample design, not real-world probabilities. The package supports
the endpoint comparison; it does not include code, annual trajectories, or a
complete replication archive.


Selected 90% attainment region (inclusive bounds; see SI):
- gA: -0.0299987863903544 to -0.00209324714768967
- rEI: 0.0263328813446942 to 0.0499987921899697
- rho: 0.69344855109361 to 0.899956486126203
- s_max: 0.651950503933822 to 0.999942321111727
At saved precision, 162 of 244 sampled futures within these bounds meet
the 90% benchmark (66.4%), compared with 293 of 10,000 overall.

Public calibration sources (not bundled)
BITRE domestic aviation activity time series:
https://catalogue.data.infrastructure.gov.au/dataset/australian-domestic-airline-activity-time-series
Australian Energy Statistics 2025, Table F:
https://www.energy.gov.au/publications/australian-energy-update-2025
