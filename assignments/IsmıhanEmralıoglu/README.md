# Ab Initio Structure Prediction of Tumor Suppressor Protein BRCA1

**Author:** İsmihan EMRALİOĞLU  
**Institution:** Inonu University – Department of Molecular Biology and Genetics  
**Course:** Molecular Modeling  

---

## Project Overview

This project focuses on the *ab initio* three-dimensional (3D) structure prediction of the BRCA1 protein RING domain using AlphaFold 3. BRCA1 is a critical tumor suppressor protein involved in DNA repair, maintenance of genome stability, and regulation of the cell cycle.

Because the full-length BRCA1 protein is large and contains partially unresolved experimental regions, computational structural prediction offers valuable insight into its functional domains and interaction mechanisms.

---

## Methodology

The structural prediction was performed using **Google DeepMind AlphaFold 3**.

- Target Protein: **BRCA1 RING Finger Domain**
- UniProt ID: **P38398**
- Prediction Type: **Monomeric structure**
- Total Generated Models: **5**

Among the generated conformations, **model_2** was selected as the reference structure due to its superior confidence scores and structural consistency.

Structural confidence analysis included:
- pLDDT confidence scoring
- pTM score evaluation
- Predicted disorder analysis
- PAE (Predicted Aligned Error) matrix assessment

---

## Structural Analysis and Visualization

The predicted `.cif` structure was imported into **PyMOL** for structural visualization and confidence mapping.

Residues were colored according to per-residue pLDDT confidence values:

| Confidence Level | Color | Interpretation |
|---|---|---|
| pLDDT > 90 | Blue | Highly stable α-helix and β-sheet core regions |
| 90 > pLDDT > 50 | Cyan / Yellow | Moderately flexible loop regions |
| pLDDT < 50 | Orange | Low-confidence or intrinsically disordered regions |

The central zinc-binding core exhibited strong structural confidence, while peripheral loops showed increased flexibility.

---

## Highlighted Functional Region

In the PyMOL render (`brca1_pymol_render.png`), zinc-coordinating cysteine and histidine residues within the RING domain were highlighted as **green spheres** to emphasize their importance in ubiquitin ligase activity and protein–protein interactions.

These residues are essential for maintaining the structural integrity and biological activity of the BRCA1 RING domain.

---

## Repository Contents

| File Name | Description |
|---|---|
| `fold_brca1_model_model_2.cif` | Predicted 3D structural model of the BRCA1 RING domain |
| `fold_brca1_model_summary_confidences_2.json` | Structural confidence metrics including pLDDT and PAE data |
| `brca1_pymol_render.png` | PyMOL visualization with confidence coloring and highlighted functional residues |

---

## Conclusion

The AlphaFold-based *ab initio* prediction successfully generated a structurally reliable model of the BRCA1 RING domain.

The predicted structure revealed:
- A stable zinc-binding core region
- Well-defined secondary structural elements
- Flexible peripheral loop regions

These observations are consistent with the functional role of BRCA1 in DNA repair and ubiquitin-mediated signaling pathways.

This study demonstrates how AI-driven computational modeling can provide meaningful structural insight into biologically important protein domains with limited experimentally resolved structural data.
