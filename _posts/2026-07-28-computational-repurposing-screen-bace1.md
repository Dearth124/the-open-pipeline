---
title: "Computational Repurposing Screen of FDA-Approved Anti-Inflammatory and Antiviral Drugs Against BACE1 (β-Secretase 1): A Blind Molecular Docking Study"
author: Sanav Kumar
pdf: /assets/papers/BACE1_repurposing_paper_AJSR.pdf
---

**Abstract.** Beta-secretase 1 (BACE1) is the rate-limiting enzyme in amyloid-beta production and a genetically validated drug target for Alzheimer's disease, yet every purpose-built BACE1 inhibitor to reach Phase 2/3 clinical trials (verubecestat, lanabecestat, atabecestat, umibecestat, and elenbecestat) has failed on grounds of futility, hepatotoxicity, or cognitive worsening. This creates a rationale for exploring drug repurposing rather than de novo inhibitor design. This study screened 36 FDA-approved compounds from two mechanistically underexplored classes — anti-inflammatory drugs (n = 20) and antivirals (n = 16) — against a high-confidence AlphaFold structure of human BACE1 (UniProt P56817; pLDDT 87.48) using blind molecular docking (CB-Dock2 / AutoDock Vina). The docking method was validated by reproducing a literature Vina score for the clinical BACE1 inhibitor atabecestat (−9.61 kcal/mol against PDB 1FKN), and all 36 compounds independently redocked to a single dominant cavity whose contact-residue list included both catalytic aspartates in every case. The six HIV-1 protease inhibitors in the library occupied five of the top eight ranks overall, each meeting or approaching the atabecestat benchmark — a result consistent with the shared aspartic-protease catalytic mechanism of BACE1 and HIV-1 protease.

## Why BACE1, and why repurposing

Alzheimer's disease affects an estimated 7.2 million people aged 65 and older in the U.S. alone, a number projected to reach 13.8 million by 2060. The amyloid cascade hypothesis points to BACE1 as the rate-limiting enzyme in amyloid-beta production, making it a genetically validated, mechanistically central drug target. But every purpose-built BACE1 inhibitor to reach late-stage trials — verubecestat, lanabecestat, atabecestat, umibecestat, elenbecestat — has failed, several after causing cognitive worsening. That pattern motivated a different approach here: instead of designing a new molecule from scratch, screen drugs that are *already* FDA-approved and see whether any bind the BACE1 active site well enough to be worth a second look.

Two lines of evidence pointed toward anti-inflammatory drugs and antivirals specifically. Epidemiological studies have long associated long-term NSAID use with reduced Alzheimer's risk. And structurally, BACE1 belongs to the aspartic protease family — the same family as HIV-1 protease — which share a conserved catalytic mechanism built around a dyad of active-site aspartate residues. Inhibitor scaffolds that work against one family member have historically transferred to others.

## Method, in brief

A high-confidence AlphaFold structure of human BACE1 (pLDDT 87.48) was used as the docking target. Active-site residues (the catalytic dyad, flap loop, and substrate-binding subpockets) were identified from the published structural biology literature and cross-referenced across numbering conventions. A 36-compound library — 20 anti-inflammatory drugs and 16 antivirals, including all six clinically available HIV-1 protease inhibitors — was docked blind (no predefined binding site) against the structure using CB-Dock2/AutoDock Vina. Seven of the initial 36 SMILES structures turned out to describe the wrong molecule despite being syntactically valid, and were caught and corrected via a molecular-formula/weight cross-check before docking.

Two validation checks anchored the results: re-docking the known clinical inhibitor atabecestat against a real BACE1 crystal structure to confirm the scoring was in a sane range, and confirming that every top-ranked docking pose actually contacted both catalytic aspartates rather than some arbitrary surface pocket.

## What came out on top

The six HIV-1 protease inhibitors dominated the ranking: lopinavir (−10.6 kcal/mol), saquinavir (−10.1), darunavir (−9.6), nelfinavir (−9.5), atazanavir (−9.2), and ritonavir (−8.9) — five of the top eight compounds overall, each within reach of the atabecestat benchmark. These six drugs were developed independently by different companies over roughly two decades, sharing only their original target and a large, peptidomimetic pharmacophore — which makes their convergence on this result more interesting than if a single standout compound had scored well.

Montelukast, a leukotriene-receptor antagonist better known as an asthma drug, was the strongest performer outside the protease-inhibitor class (−9.0 kcal/mol), through what looks like a distinct shape-complementarity mechanism rather than the transition-state mimicry driving the protease inhibitor results. Among the NSAIDs, a clean gradient emerged tracking heteroaromatic/sulfonamide content rather than drug subclass: celecoxib and piroxicam scored well; aspirin and ibuprofen did not. Small polar nucleoside analogs and rigid cage amines (acyclovir, ribavirin, amantadine, and similar) consistently scored worst.

## What this does and doesn't show

Docking scores are a hypothesis-generating, rank-ordering tool — not a measurement of true binding affinity, and not proof that any of these drugs would work in a patient. This screen used a single static predicted structure and an automated cavity detector, has no experimental (enzymatic or structural) validation yet, and HIV protease inhibitors are known to have limited blood-brain-barrier penetration, which would be a real obstacle for any CNS application regardless of docking score. What it does provide is a structurally rationalized, testable hypothesis: the shared aspartic-protease catalytic mechanism between BACE1 and HIV-1 protease is a plausible reason these six drugs cluster at the top, and it's now a specific, falsifiable claim that enzymatic assays could confirm or rule out.

The full methods, complete 36-compound ranking table, and references are in the paper linked above.
