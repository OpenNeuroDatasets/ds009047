# Dizziness / Vertigo MRI and Clinical Dataset

## Overview

This dataset contains structural brain MRI and associated clinical phenotype data for 477 participants from a retrospective dizziness and vertigo cohort.

Each participant is identified by a de-identified BIDS identifier (`sub-XXX`). The released imaging data include T1-weighted, T2-weighted, and FLAIR MRI.

## Dataset contents

- `participants.tsv`: participant-level demographic information.
- `phenotype/clinical.tsv`: selected hospitalization and discharge variables.
- `phenotype/blood.tsv`: hematology measurements.
- `phenotype/biochemical.tsv`: biochemical laboratory measurements.
- `phenotype/ecg.tsv`: electrocardiographic findings.
- `sub-XXX/anat/`: T1-weighted, T2-weighted, and FLAIR MRI with JSON sidecars.

## Temporal representation

Absolute clinical and imaging dates are not included in the public dataset.

MRI acquisition day is defined as day 0. In `phenotype/clinical.tsv`:

- `admission_day` is the hospital admission day relative to MRI acquisition.
- `discharge_day` is the hospital discharge day relative to MRI acquisition.

Negative values indicate days before MRI and positive values indicate days after MRI.

## Privacy

Participant identifiers are de-identified and do not encode source identifiers.

Ages above 89 years are top-coded to 89.

Scanner identifiers in imaging JSON sidecars are pseudonymized. Institution-related fields are de-identified. Absolute acquisition dates and times, patient names, birth dates, accession numbers, and source DICOM identifiers are not included in the public release.

The source DICOM data are not part of this public dataset.

## Phenotype coding

The clinical phenotype includes a standardized English label for the main discharge diagnosis together with ICD-10 coding where available.

ECG findings are provided as standardized English findings, with ICD-10 codes where applicable.

Missing values are represented as `n/a`.

## Imaging

Each released participant has:

- one T1-weighted MRI
- one T2-weighted MRI
- one FLAIR MRI

Image acquisition metadata are provided in the corresponding JSON sidecars where available.


