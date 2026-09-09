# 4i, explained interactively

An interactive walkthrough of the chemistry behind **iterative indirect immunofluorescence imaging (4i)** — what bonds form at each step, what the elution buffer actually breaks, and why the fixed cells can survive being chemically stripped multiple times.

**[▶ Open the explainer](https://laelise.github.io/4i-explainer/)**

<!-- Add a screenshot or GIF here once you have one:
![Screenshot of the elution step](docs/elution.png)
-->

---

## Why this exists

When I first learned 4i, I focused on cranking out data and learning the wet lab steps as fast as possible, so I neglected the chemistry behind the method. Over time, I started noticing small details in my methodology that affected how the next elution turned out. So I started exploring the chemistry and what is actually happening to make 4i possible. Knowing the chemistry behind it all has helped me run cleaner experiments and remind myself not to be lazy with measurements (aka, the "that's close enough" mindset), which has made the difference between getting 15-20 features instead of only 7-10 on my samples. 

In a PFA-fixed sample, the antigen is held in place by **covalent** methylene bridges, while the antibody is held on by **non-covalent** affinity alone. The elution buffer is built to break one and not the other. This interactive walkthrough lets you watch that asymmetry happen.

## What's in it

Ten steps, from live cell through analysis. Each one pairs a molecular animation with the specific chemistry involved.

What I want to highlight is **step 8**. Elution gets three independent controls — chaotrope, pH, and TCEP — and each one only breaks its own class of bond:

| Reagent | What it breaks |
|---|---|
| Urea + guanidinium (~2.4 M each) | Hydrogen bonds; collapses the hydrophobic effect |
| Glycine-HCl, pH 2.5 | Salt bridges — every Asp and Glu is protonated |
| TCEP, 70 mM | Interchain disulfides, so the IgG can't refold and rebind |

Turn up chaotrope alone, and the salt bridges still hold. Add acid and those go, but the antibody stays assembled. Only with all three does it come apart and wash off — while the amber methylene bridges never move.

Press **X** at any point to dim everything non-covalent and leave only the permanent bonds lit.

## Running it

It's a single self-contained HTML file. No build step, no dependencies, no network access required.

```bash
git clone https://github.com/laelise/4i-explainer.git
cd 4i-explainer
open index.html          # or just double-click it
```

Keyboard: `←` `→` to step, `X` for covalent-only, `F` for full screen, `Esc` to close the About panel.

## Using the figures

**Export SVG** downloads whatever is currently on screen, with the slider positions baked in. SVG opens natively in Illustrator, Inkscape, and Affinity with every path and text object still editable — so you can export the elution step at three different slider settings and restyle them into a figure panel.


## About the method

4i was developed in the **Pelkmans lab** at the University of Zurich. This repository is an independent educational illustration of their published method. It is not affiliated with or endorsed by its authors.

> Gut G, Herrmann MD, Pelkmans L. Multiplexed protein maps link subcellular organization to cellular states. *Science*. 2018;361(6401):eaar7042. https://doi.org/10.1126/science.aar7042

> Kramer BA, Sarabia del Castillo J, Pelkmans L, Gut G. Iterative Indirect Immunofluorescence Imaging (4i) on Adherent Cells and Tissue Sections. *Bio-protocol*. 2023;13(13):e4712. https://doi.org/10.21769/BioProtoc.4712

The official analysis code from the 2018 paper is at [pelkmanslab/4iImageAnalysisAndMultiplexedProteinMaps](https://github.com/pelkmanslab/4iImageAnalysisAndMultiplexedProteinMaps).

## Scope and limitations

Every scene is a **schematic of interaction classes, not a structural model.** Bond geometry, antibody pose, epitope shape, and organelle placement are illustrative. Do not read CDR geometry or stoichiometry off these drawings.

Buffer concentrations shown on the elution controls are the published working values. The repository contains **no experimental data** of any kind.

## Author

Built by **Lauryn Elise Bailey** — [Purvis Lab](https://www.med.unc.edu/genetics/purvislab/), Department of Genetics, UNC-Chapel Hill.

| | |
|---|---|
| Email | [lbailey@unc.edu](mailto:lbailey@unc.edu) |
| LinkedIn | [in/laurynelisebailey](https://www.linkedin.com/in/laurynelisebailey) |
| GitHub | [@laelise](https://github.com/laelise) |
| Lab | [med.unc.edu/genetics/purvislab](https://www.med.unc.edu/genetics/purvislab/) |

## Citing this

If it's useful in a talk or a course, a link with the author's name is plenty. If you'd rather cite it formally, see `CITATION.cff` — GitHub renders a "Cite this repository" button from it.

> Bailey LE. *4i, explained interactively.* 2026. https://laelise.github.io/4i-explainer/

Please cite the papers above for the method itself.

## License

Code is MIT (see `LICENSE`). The explanatory text and diagrams are CC BY 4.0 — use them, adapt them, just keep the attribution.
