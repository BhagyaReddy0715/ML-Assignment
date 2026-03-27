## What This Tutorial Covers

This tutorial explains **Batch Normalisation (BN)** — the technique that made training deep neural networks practical. It covers the problem it solves (internal covariate shift), the four-step algorithm derived from scratch, running statistics for inference, and quantitative comparison on CIFAR-10.

**You will learn:**
- What internal covariate shift is and why it slows training
- The four-step BN algorithm (mean, variance, normalise, scale+shift)
- Why γ and β learnable parameters are essential
- How running statistics work for inference
- The most common BN bug: forgetting `model.eval()`
- When to use BN vs LayerNorm vs InstanceNorm

---

## Files in This Folder

| File | Description |
|------|-------------|
| `batch_normalisation_tutorial.ipynb` | Full Jupyter notebook with all code, figures, and explanations |
| `batch_normalisation_tutorial.docx` | Word tutorial document (under 2000 words) |
| `README.md` | This file |
| `LICENSE` | MIT Licence |

---

## How to Run the Notebook

### Requirements
```bash
pip install numpy matplotlib
```

### Steps
1. Clone or download this repository
2. Open a terminal in this folder
3. Run:
```bash
jupyter notebook batch_normalisation_tutorial.ipynb
```
4. Run all cells in order (Cell → Run All)

> **Note:** This notebook uses only NumPy and Matplotlib no PyTorch or heavy framework required. The BN algorithm is implemented from scratch for maximum clarity.

---

## Figures Produced

| Figure | Description |
|--------|-------------|
| `fig1_covariate_shift.png` | Internal covariate shift + loss landscape effect |
| `fig2_bn_algorithm.png` | BN transformation stages + training speed comparison |
| `fig3_bn_placement.png` | Original vs pre-activation BN + normalisation variants |
| `fig4_bn_benefits.png` | LR sensitivity + implicit regularisation effect |
| `fig5_running_stats.png` | Running statistics convergence + train/eval mode impact |

---

## Accessibility

All figures use:
- **Colourblind-safe palettes** (teal/coral scheme throughout)
- **Hatch patterns** on bar charts alongside colour
- **Solid/dashed/dotted/dash-dot line styles** to distinguish series
- **Shaded regions** to highlight train-test gaps
- **Descriptive alt-text captions** in notebook markdown cells
- **Structured headings** (H1/H2) for screen reader navigation

---

## References

1. Ioffe, S. and Szegedy, C. (2015) 'Batch normalization: Accelerating deep network training by reducing internal covariate shift', *ICML 2015*, pp. 448–456. https://arxiv.org/abs/1502.03167  
2. Ba, J.L., Kiros, J.R. and Hinton, G.E. (2016) 'Layer normalization', arXiv:1607.06450. https://arxiv.org/abs/1607.06450  
3. Santurkar, S., Tsipras, D., Ilyas, A. and Madry, A. (2018) 'How does batch normalization help optimization?', *NeurIPS 31*. https://arxiv.org/abs/1805.11604  
4. He, K., Zhang, X., Ren, S. and Sun, J. (2016) 'Identity mappings in deep residual networks', *ECCV 2016*. https://arxiv.org/abs/1603.05027  
5. Krizhevsky, A. (2009) Learning multiple layers of features from tiny images. University of Toronto. https://www.cs.toronto.edu/~kriz/cifar.html  

---

## Licence

This project is licensed under the **MIT Licence** — see [LICENSE](LICENSE) for details.

---


