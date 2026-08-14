# Gut Microbiome Comparison: Health vs. Crohn's Disease

> Comparing gut bacterial genus abundance between healthy individuals and Crohn's disease patients using curated microbiome data.

---

## Overview

This project compares the relative abundance of six key gut bacterial genera between healthy individuals and people with Crohn's disease, using curated, quality-controlled microbiome data. It explores how the gut bacterial community shifts in inflammatory bowel disease and what that might mean biologically.

---

## Background

The gut microbiome is the community of bacteria (and other microbes) living in the human digestive tract. A healthy, balanced microbiome plays a role in digestion, immune regulation, and keeping the gut lining calm. Crohn's disease is a chronic inflammatory bowel disease that causes inflammation in the digestive tract, and it has been repeatedly linked to changes in gut bacterial composition, a state often called dysbiosis.

This topic is relevant because understanding how the microbiome shifts in disease could eventually help with diagnosis, treatment, or even microbiome based therapies. It also connects directly to earlier projects in this series, moving from single genes to whole bacterial communities.

---

## Objective

The aim of this project is to:

- Compare relative abundance of key gut bacterial genera between healthy and Crohn's disease samples
- Identify which genera increase, decrease, or stay roughly the same in Crohn's disease
- Visualize the comparison clearly
- Interpret the biological meaning of the observed shifts, while being honest about what the data can and cannot show

---

## Research Question

How does the relative abundance of key gut bacterial genera differ between healthy individuals and people with Crohn's disease?

---

## Dataset / Data Source

- **Source:** GMrepo (Data Repository for Human Gut Microbiota)
- **Organism:** Human gut microbiome (bacterial genera)
- **Database:** gmrepo.humangut.info
- **File format:** TSV (tab-separated values), genus-level abundance stats for Health and Crohn Disease phenotypes

---

## Tools & Technologies

- Python
- Google Colab (Jupyter Notebook)
- Pandas
- NumPy
- Matplotlib
- Git
- GitHub

---

## Methodology

1. **Data collection:** Downloaded curated genus-level abundance stats for Health and Crohn Disease phenotypes from GMrepo.
2. **Data preprocessing:** Loaded both TSV files with pandas and filtered them down to six genera present in both datasets, matched by NCBI taxon ID.
3. **Analysis:** Compared mean relative abundance of each genus between the Health and Crohn's groups.
4. **Visualization:** Built a grouped bar chart in Python (matplotlib) comparing each genus side by side.
5. **Interpretation:** Explained the biological meaning of the shifts, and the limitations of abundance-only comparisons.

---

## Results

Six gut bacterial genera were compared between healthy individuals and Crohn's disease patients:

| Genus | Health (mean %) | Crohn's (mean %) | Direction |
|---|---|---|---|
| Bacteroides | 14.56 | 20.13 | Higher in Crohn's |
| Bifidobacterium | 7.05 | 4.55 | Lower in Crohn's |
| Blautia | 3.94 | 4.00 | Roughly equal |
| Clostridium | 0.40 | 0.72 | Higher in Crohn's |
| Faecalibacterium | 4.25 | 4.29 | Roughly equal |
| Roseburia | 2.14 | 3.25 | Higher in Crohn's |

**Figure 1.** Grouped bar chart comparing relative abundance of six gut bacterial genera between healthy individuals (green) and Crohn's disease patients (red), generated in Python using matplotlib.

![Microbiome comparison chart](gut_microbiome_health_vs_crohns.png)

---

## Biological Interpretation

Looking at this chart, the first thing that stands out is Bacteroides. It's noticeably higher in Crohn's samples than healthy ones, which honestly surprised me a bit since I expected disease to mean less bacteria overall, not more of something.

Bifidobacterium tells a different story though, it drops in Crohn's. This one actually makes sense with what's known about it, Bifidobacterium is generally considered a "good" genus, it helps produce compounds that keep the gut lining calm and reduce inflammation. So seeing it go down in a disease that's literally about gut inflammation checks out.

Blautia and Faecalibacterium barely change between the two groups, so those don't seem to be strongly linked to Crohn's, at least not in this data. Clostridium and Roseburia both go up a bit in Crohn's, but Roseburia is interesting because it's also usually considered a helpful genus, so seeing it increase instead of decrease doesn't fit the simple "good bacteria down, bad bacteria up" story I was expecting.

I think the honest takeaway here is that Crohn's isn't just about one bacteria increasing or decreasing, it's more of a shift in the whole balance of the gut community. When something like Bifidobacterium drops, other genera might just expand into that space, not necessarily because they're causing the disease, but because there's less competition. This data can't really tell us what's cause and what's effect, it just shows that the balance looks different between healthy people and people with Crohn's. To actually know what's driving what, you'd need a different kind of study, not just abundance comparisons like this one.

---

## Repository Structure

```
Gut-Microbiome-Health-vs-Crohns/
│
├── microbiome_comparison.ipynb
├── gut_microbiome_health_vs_crohns.png
├── README.md
└── LICENSE
```

---

## Limitations

- Only six genera were compared out of hundreds present in the full dataset; the broader picture may look different.
- Genus-level data can hide important differences at the species level, where some species within a genus may be protective and others harmful.
- This is an abundance comparison only; it cannot establish whether these shifts cause Crohn's disease or result from it.
- Data was pooled from GMrepo's curated samples, which come from many different studies and populations, introducing variability not controlled for here.

---

## Future Work

Possible improvements:

- Expand the comparison to more genera, or move to species-level data
- Include additional disease states (e.g. Ulcerative Colitis) for a broader comparison
- Calculate alpha and beta diversity metrics for a more complete community-level picture
- Look into longitudinal data to see how microbiome composition changes over the course of disease progression or treatment

---

## Learning Outcomes

Through this project I gained experience in:

- Bioinformatics
- Data analysis
- Scientific documentation
- GitHub
- Python programming

---

## Key Skills Demonstrated

- Biological data interpretation
- Scientific literature review
- Python programming
- Data visualization
- Reproducible research
- Git & GitHub

---

## Disclaimer

This project was developed as an educational and portfolio project. AI-assisted tools were used to support coding and documentation. The project was reviewed, validated, organized, and interpreted by the author.

---

## Author

**Zeophuen Sahoo**

GitHub: https://github.com/Zeophuen

---

## License

This project is licensed under the MIT License.
