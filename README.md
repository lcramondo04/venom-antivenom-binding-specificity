# Comparing the Venom Proteins of Phylogenetically Close and Distant Species

**Christian Gramajo, Brooke Patrick, Lucas Ramondo, Henry Seeger**
Bioinformatics and Computational Biology (BCB) & Biology and Biotechnology (BBT), Worcester Polytechnic Institute
*Bioinformatics*, 2025 (submitted)

📄 [Full Paper (PDF)](./paper/Bioinfomatics_Final_Paper_Formatted.pdf)

## Overview

Snakebite envenoming affects roughly 2 million people per year, and current antivenom treatments are highly species-specific — a major bottleneck when treatment speed matters and the biting species is often unknown. This project investigated whether antivenom antibodies developed for one snake species can effectively bind venom proteins from phylogenetically related species, which could point toward more broadly effective antivenom treatments.

We tested the hypothesis that binding specificity between an antivenom and a venom protein correlates with the phylogenetic proximity of the two species.

## Approach

- Sourced novel venom protein candidates from SCOP, Venom Zone, and prior literature (Torres et al., Ahmadi et al.), selecting proteins across a range of phylogenetic distances from three validated antivenom controls
- Built a maximum-likelihood phylogenetic tree (MEGA12) to quantify evolutionary distance between venom protein sequences
- Modeled antivenom–venom protein complexes with **AlphaFold Multimer**, scoring predictions via pLDDT, ptm, and iptm
- Ran **HADDOCK 2.4** docking simulations on control complexes to validate binding realism (HADDOCK score, RMSD, van der Waals/electrostatic energy, Z-score)
- Scored complexes with **Rosetta** (total score, fa_atr, fa_elec, dslf_fa13) for additional binding stability comparison
- Visualized and superimposed predicted structures against control complexes in **UCSF ChimeraX**

## Key Findings

- All three control antivenom–venom pairs showed high binding affinity across every method used, validating the overall pipeline
- Novel venom proteins closer to the control species on the phylogenetic tree generally scored higher for antivenom binding, partially supporting the hypothesis
- One more distantly related species unexpectedly scored higher than several closer relatives — and higher than some controls — suggesting binding specificity isn't fully explained by phylogenetic distance alone
- Results were directionally supportive but not statistically sufficient to confirm the hypothesis; the authors note a larger protein/species sample size is needed

## Tools & Techniques

AlphaFold Multimer, HADDOCK 2.4, Rosetta, UCSF ChimeraX, MEGA12 (phylogenetics), UniProt / SCOP / Venom Zone databases

## Future Work

- Expanding to a wider range of antivenom and venom proteins beyond the three synthetic controls used here
- Using Rosetta more extensively in place of HADDOCK for faster, higher-throughput analysis
- Incorporating Schrödinger software for more rigorous docking validation

---
*Bioinformatics and Computational Biology Program, Worcester Polytechnic Institute. Associate Editor: Prof. Dimitry Korkin.*
