# ScaleMAP

ScaleMAP is a nonlinear dimensionality reduction technique related to UMAP that correctly represents the underlying scale of the data. Particularly useful in transcriptomics, hyperspectral imaging, and flow cytometry, where UMAP's scale distortion misses features. See the [arXiv paper](https://arxiv.org/abs/2605.30597) for more.

This package is currently a quick release. It is derived from `umap-learn` and keeps essentially the same interface.

## Installation

```bash
pip install scalemap
```

## Usage

```python
import scaleMAP

mapper = scaleMAP.UMAP(scalemap=True, scale_lambda=1.0)
embedding = mapper.fit_transform(data)
```

The distribution name on PyPI is `scalemap`; the import package is `scaleMAP`.
If you don't set scalemap=True, it will behave just like UMAP. 
scale_lambda=1.0 sets the scaleMAP behavior to be fully on. You can interpolate between fully on and fully off by setting values between 0.0 and 1.0.

## Citation

If you use ScaleMAP in scientific work, please cite the arXiv paper:

> Poorna, R. & Cicerone, M. T. (2026). ScaleMAP: Preserving Local Density and Neighborhood Structure in Low-Dimensional Embeddings. arXiv:2605.30597. https://arxiv.org/abs/2605.30597

```bibtex
@article{poorna2026scalemap,
  title={ScaleMAP: Preserving Local Density and Neighborhood Structure in Low-Dimensional Embeddings},
  author={Poorna, Rajas and Cicerone, Marcus T.},
  journal={arXiv preprint arXiv:2605.30597},
  year={2026},
  url={https://arxiv.org/abs/2605.30597}
}
```

## Attribution

ScaleMAP is derived from `umap-learn` by Leland McInnes and contributors. The upstream project is available at:

https://github.com/lmcinnes/umap

The upstream UMAP package is BSD 3-Clause licensed. ScaleMAP is distributed under the same license. See `LICENSE` and `NOTICE.md`.

Please also cite the original UMAP work if appropriate:

```bibtex
@article{mcinnes2018umap-software,
  title={UMAP: Uniform Manifold Approximation and Projection},
  author={McInnes, Leland and Healy, John and Saul, Nathaniel and Grossberger, Lukas},
  journal={The Journal of Open Source Software},
  volume={3},
  number={29},
  pages={861},
  year={2018}
}
```
