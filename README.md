# RootEx 2.0

A compact map of the **RootEx** pipeline, with pointers to the two GitHub repositories, the dataset, and papers.

```
[Data & Annotations] → (Deep Model: multi-head DeepLabV3+) → [Root/Tip/Source masks]
                                               ↓
                      (Post-DL: Graph → Path selection → RSML + (optional) GT metrics)
```

---

## Repositories

- **Part 1 — Deep Model (Training & Inference):**  
  Multi-head DeepLabV3+ for roots, tips, sources (produces the `.pth` and inference masks).  
  👉 https://github.com/MaicholD95/RootEx2.0_DeeplabV3Plus

- **Part 2 — Post-DL (Graph → Paths → RSML):**  
  Skeletonization, graph building/refinement, tip→source path selection, **GT-optional** evaluation, and RSML export.  
  👉 https://github.com/MaicholD95/RootEx2.0_GetRsml (use this after obtaining the `.pth` from Part 1).

---

## Dataset

- **TILLMore-CDC** (images, masks/labels, and GT resources where applicable)  
  👉 https://github.com/MaicholD95/TILLMore-CDC

Use the dataset to train Part 1 and to test/evaluate Part 2 (with or without GT).

---

## Quickstart (End-to-End)

1. **Train / obtain checkpoint** (`.pth`) with Part 1 (DeepLabV3+).  
2. **Run Part 2** with your test set:
   - Build skeleton & graph, snap tips/sources, enumerate and select paths
   - (Optional) Compare with GT graphs and compute metrics
   - Export **RSML** per image

> Tip: thresholds (root/tip/source) and separation parameters (sigma, radii) should match the scale of your data.

---

## Papers & Citation

- **RootEx 2.0** — *in press at* **Expert Systems with Applications (ESWA)**.  
  *(Add DOI/BibTeX here when available.)*

If you use this pipeline, please cite **RootEx 2.0**. You can also reference the dataset (**TILLMore-CDC**) in your work.

---

## Contact

For issues or questions, please open a GitHub issue in the relevant repository.

