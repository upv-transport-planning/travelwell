# Nature Cities — Mplus reproducibility package

## Purpose
This package consolidates the Mplus syntax and available Mplus outputs underlying the reported psychometric, measurement-invariance, structural and multilevel sensitivity analyses in the manuscript on street-design attributes, affect and scenario-specific travel satisfaction. The INTERNAL version additionally contains the final anonymous analysis files required to rerun the models.

## Software
Analyses were specified for Mplus 9.1. IBM SPSS Statistics 26 was used for descriptive reliability/factorability analyses reported elsewhere; those SPSS computations are not part of this Mplus package.

## Final analysis samples
- Scenario A: 492 participants, 1,968 long-format records.
- Scenario B: 627 participants, 2,508 long-format records.
- `online`: 1 = online; 2 = face-to-face.
- `MODO_rango`: 1 = walking; 2 = cycling; 3 = e-scooter.
- `V1`: exact age; `V3`: 1 woman / 2 man; `V14`: travel frequency; `V15`: trip duration.
- `-999` is the missing-value code where applicable.

The legacy-order files in the INTERNAL archive are mechanical column reorderings of the final short-format data used only so that the rerun S3/S4 syntax matches the variable order embedded in the recovered historical Mplus setup. No participant or response values were changed.

## Code-to-reporting map
- `01_S3_affect_CFA_ESEM`: Supplementary Table S3. Reconstructed from original outputs, rerun with final samples and validated.
- `02_S4_travel_satisfaction_CFA`: Supplementary Table S4. Reconstructed, rerun with final samples and validated.
- `03_primary_SEM_S5_S9_S10`: Supplementary Tables S5, S9 and S10, Fig. 2 and primary Results. Original final syntax/output recovered.
- `04_S6_survey_method_invariance`: Supplementary Table S6. Original exact syntax was not recovered; final syntax was reconstructed from the recovered workflow, rerun on the final samples and validated exactly against all reported fit statistics and robust difference tests. See `S6_VALIDATION_RECORD.txt`.
- `05_S7_travel_mode_invariance`: Supplementary Table S7. Original final syntax/output recovered.
- `06_S8_sex_invariance`: Supplementary Table S8. Scenario A uses the stable reduced cross-loading specification; Scenario B retains both cross-loadings. Original final syntax/output recovered.
- `07_S11_survey_method_structural`: Supplementary Table S11 and survey-method sensitivity paragraph. Reconstructed, rerun and explicitly adopted as final.
- `08_S12_travel_mode_structural`: Supplementary Table S12 and Fig. 3. Includes global and pairwise Wald specifications.
- `09_S13_sex_structural`: Supplementary Table S13 and sex panel in Fig. 4.
- `10_S14_age_moderation`: Supplementary Table S14 and age panel in Fig. 4.
- `11_S15_trip_duration`: Supplementary Table S15 and trip-duration panel in Fig. 4.
- `12_S16_travel_frequency`: Supplementary Table S16 and travel-frequency panel in Fig. 4.
- `13_S17_repeated_measurement_invariance`: repeated-evaluation configural, metric, scalar and targeted partial-scalar measurement-invariance analyses across the four within-participant evaluations. Intended for Supplementary Table S17. The folder preserves the full model sequence, including diagnostic contrast-specific scalar models and the retained final partial-scalar solutions.
- `14_S18_multilevel_sensitivity`: ICC diagnostics and within-focused two-level SEM sensitivity analyses separating within-participant from between-participant variation. Intended for Supplementary Table S18. Preliminary improper between-level models are retained in a clearly labelled diagnostic subfolder; the final reported refits are in `02_final_refit`.

## Provenance
The `MANIFEST.csv` file identifies whether each model was recovered from original analysis files or reconstructed/rerun. `SHA256SUMS.txt` provides file-level integrity hashes.

## Validation status
S3, S4, S6 and S11 were reconstructed where needed and rerun against the final analysis data. S6 now reproduces the previously reported statistics exactly, so there is no remaining S6 validation item. Other original folders contain the recovered final syntax/output used for the reported analyses.

The additional repeated-evaluation invariance analyses support configural and approximate metric invariance in both scenarios, with scalar or targeted partial-scalar invariance retained for all construct-by-scenario blocks. The final multilevel sensitivity analyses use ICC diagnostics plus a within-focused two-level latent SEM with a saturated observed-variable between level; their within-person total associations closely reproduce the primary cluster-adjusted results. See the analysis records in folders 13 and 14.

## Data-sharing note
The INTERNAL archive contains anonymous analysis files for internal reproducibility checking. A separate code-only archive excludes participant-level analysis files. The new repeated-evaluation analyses require the final short-format files and the multilevel sensitivity analyses require the final long-format files listed in `data/README_DATA_REQUIRED.txt`. Whether participant-level data are placed in a public repository should be decided separately under the final Data Availability and ethics/data-sharing position for the manuscript.
