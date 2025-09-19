# When colder is better: Thermal performance trade-offs enable physiological resilience in upwelling-adapted Galápagos cnidarians
This repository contains the data, metadata, and R code used to quantify the thermal performance of Galápagos cnidarians

**Study Description**: Understanding how temperature governs biological systems is increasingly urgent under climate change. For sessile ectotherms unable to track shifting thermal gradients, localized adaptation may be critical for persistence. Thermal performance curves describe the relationship between temperature and metabolic fitness, but species can exhibit different temperature–performance associations depending on environmental conditions and physiological traits. Classical theory, including the ‘hotter-is-better’ hypothesis, predicts organisms adapted to warmer environments achieve higher maximal performance (*P*<sub>max</sub>) at elevated thermal optima (*T*<sub>opt</sub>). While this pattern is well documented in terrestrial taxa, marine evidence remains inconsistent. We quantified respiration across a 20–36°C gradient for four Galápagos ahermatypic cnidarians: two octocorals (*Pacifigorgia* *darwinii*, *Muricea* *plantaginea*), the cup coral *Tubastraea* *coccinea*, and the sea anemone *Bunodosoma* *grande*. Based on thermal histories and morphologies, we predicted octocorals, would show lower *T*<sub>opt</sub> and *P*<sub>max</sub> compared to warm-adapted species. Contrary to expectations, cooler-adapted octocorals exhibited lower *T*<sub>opt</sub> (33.3–35.0°C) yet higher *P*<sub>max</sub> (3.8–4.0 μmol O2 g<sup>−1</sup> h<sup>−1</sup>), supporting a ‘colder-is-better’ model. This trade-off may reflect adaptation to nutrient-rich upwelling environments characteristic of the Galápagos. Findings provide evidence for alternative thermal performance models in marine ecosystems and highlight how local specialization shapes metabolic resilience, persistence, and community structure under warming. 

Keywords: adaptive traits, climate resilience, ‘colder-is-better’ hypothesis, Galápagos Archipelago, metabolic trade-offs, octocorals, thermal performance, upwelling systems

All statistical analyses were conducted in R v. 4.2.2

**Folder/File Structure & Contents**
Below contains a list of the associated datafiles and folders, woth descriptions of what lives in each:

- Cni_respiration_files: Contains species' subfolders of raw, temperature-dependent O2 measurements across the experimental temperature gradient
- Generated_rate_estimations: Contains processed, model-derived calculations of metabolic rates for each individual per species x temperature pairing
- Scripts_Rfiles: The R scripts used to process the raw data, estimate rates, perform statistical analyses, and generate plots. Also included are produced raw data files
- Cni_metadata.csv: The metadata for every individual in this study, which includes parameters like the start/stop time of each trial, chamber volume/channel, and ash free dry weight estimates
- HOBO_temperature_data.csv: Environmental temperature records used to characterize the thermal history of locations where the cnidarians reside. Data collected includes 7/28/2019 - 1/7/2022 @ 15 min intervals
- README.md: This main document, outlining the purpose, background, methods, and general information on packages and analyses




