When colder is better: Thermal performance trade-offs enable physiological resilience in upwelling-adapted Galápagos cnidarians

This repository contains the data, metadata, and R code used to quantify the thermal performance of Galápagos cnidarians.

---

STUDY DESCRIPTION

Understanding how temperature governs biological systems is increasingly urgent under climate change. For sessile ectotherms unable to track shifting thermal gradients, localized adaptation may be critical for persistence.

Thermal performance curves describe the relationship between temperature and metabolic fitness, but species can exhibit different temperature–performance associations depending on environmental conditions and physiological traits.

Classical theory, including the ‘hotter-is-better’ hypothesis, predicts organisms adapted to warmer environments achieve higher maximal performance (Pmax) at elevated thermal optima (Topt). While this pattern is well documented in terrestrial taxa, marine evidence remains inconsistent.

We quantified respiration across a 20–36°C gradient for four Galápagos ahermatypic cnidarians:

- Two octocorals (Pacifigorgia darwinii, Muricea plantaginea)
- The cup coral Tubastraea coccinea
- The sea anemone Bunodosoma grande

Based on thermal histories and morphologies, we predicted that octocorals would show lower Topt and Pmax compared to warm-adapted species.

Contrary to expectations, cooler-adapted octocorals exhibited lower Topt (33.3–35.0°C) yet higher Pmax (3.8–4.0 μmol O2 g⁻¹ h⁻¹), supporting a ‘colder-is-better’ model.

This trade-off may reflect adaptation to nutrient-rich upwelling environments characteristic of the Galápagos. Findings provide evidence for alternative thermal performance models in marine ecosystems and highlight how local specialization shapes metabolic resilience, persistence, and community structure under warming.

---

Keywords: adaptive traits, climate resilience, ‘colder-is-better’ hypothesis, Galápagos Archipelago, metabolic trade-offs, octocorals, thermal performance, upwelling systems

All statistical analyses were conducted in R v. 4.2.2

---

FOLDER/FILE STRUCTURE & CONTENTS

Below is a list of associated data files and folders with descriptions of their contents:

- Cni_respiration_files:
  Contains species-specific subfolders of raw, temperature-dependent O2 measurements across the experimental temperature gradient.

- Generated_rate_estimations:
  Contains processed, model-derived calculations of metabolic rates for each individual per species × temperature pairing.

- Scripts_Rfiles:
  R scripts used to process the raw data, estimate rates, perform statistical analyses, and generate plots. Also includes intermediate data files.

- Cni_metadata.csv:
  Metadata for each individual in this study, including trial start/stop times, chamber volume/channel, and ash-free dry weight estimates.

- HOBO_temperature_data.csv:
  Environmental temperature records (collected between 7/28/2019 – 1/7/2022 at 15-min intervals) used to characterize the thermal history of cnidarian habitats.

- README.md:
  This document, outlining the purpose, background, methods, and general information on packages and analyses.

---

HOW TO RUN / REPRODUCE THE ANALYSES

Below are step-by-step instructions to run the analyses in this repository, including configuration and assumptions. Adjust file paths or versions as needed.

1. Prerequisites:
   - Install R (version ≥ 4.4.2).
   - Install required R packages: LoLinR, nls.multstart, lme4, ggplot2, etc.
   - Set your working directory to the root of this repository so relative paths function properly.

2. Data Preparation:
   - Verify that raw respiration data files are present in the Cni_respiration_files/ folder.
   - Ensure the Cni_metadata.csv file is complete and correctly formatted.
   - Read in the raw data files to confirm proper loading and matching to metadata.

3. Rate Estimation & Analysis:
   - Run the Data_cleaning_rate_estimations.Rmd script first. This script:
     * Establishes start/end timestamps for raw respiration data
     * Normalizes data by chamber water volume, tissue weight, and background respiration
   - Then run the TPC_derivation_and_analysis.Rmd script to:
     * Fit mass-normalized rates to a modified Sharpe–Schoolfield equation
     * Derive thermal performance parameters
     * Remove outliers and run statistical analyses (e.g. linear models)
     * Assess data quality via histograms, QQ plots, and residuals

4. Reproducible Tables & Figures:
   - Both .Rmd scripts include code to generate:
     * Tables (e.g., model summaries, Tukey HSD results)
     * Figures (thermal parameter plots, TPCs by species, and a Pearson correlation between Topt and Pmax)

---

CONFIGURATION PARAMETERS

- Temperature gradient & species used in analysis
- Working directory and relative file paths
- R package versions (check for updates/compatibility)
- Outlier removal threshold: 1.5 × SD used throughout
- LoLinR parameters:
  * alpha = 0.5 (proportion of total observations)
  * Data thinning interval = every 15 seconds
