---
layout: archive
title: "📊 Graph Datasets"
permalink: /datasets/
author_profile: true
redirect_from:
  - /datasets
---

{% include base_path %}

<style>
  .dataset-table { width: 100%; border-collapse: collapse; font-size: 0.9em; margin-bottom: 30px; }
  .dataset-table th { background: #f8f9fa; color: #333; font-weight: 600; padding: 12px; border-bottom: 2px solid #dee2e6; }
  .dataset-table td { padding: 10px; border-bottom: 1px solid #eee; vertical-align: middle; }
  .tag-directed { background: #e3f2fd; color: #1976d2; padding: 2px 6px; border-radius: 4px; font-size: 0.85em; }
  .tag-undirected { background: #f1f8e9; color: #388e3c; padding: 2px 6px; border-radius: 4px; font-size: 0.85em; }
  .btn-download { background: #343a40; color: #fff !important; padding: 3px 8px; border-radius: 4px; text-decoration: none !important; font-size: 0.85em; }
  .btn-download:hover { background: #000; }
  .highlight-num { font-weight: 600; color: #d32f2f; }
  .code-section { background: #2d2d2d; color: #ccc; padding: 15px; border-radius: 6px; margin: 20px 0; }
</style>

> 💡 **Quick Access**: Most attributed datasets are available in [PyG (PyTorch Geometric)](https://pytorch-geometric.readthedocs.io/en/latest/modules/datasets.html).

---

## ⏱️ Temporal Graphs
*Dynamic networks where edges or nodes change over time.*

| Name | Source Repository | URL |
|:---|:---|:---:|
| **Network Repository** | Dynamic Graph Collection | [获取数据](https://networkrepository.com/dynamic.php){: .btn-download} |
| **SNAP** | Temporal Network Data | [获取数据](https://snap.stanford.edu/data/index.html#temporal){: .btn-download} |
| **KONECT** | Dynamic Networks | [获取数据](http://konect.cc/){: .btn-download} |
| **SocioPatterns** | Human Interaction Data | [获取数据](http://www.sociopatterns.org/datasets/){: .btn-download} |

---

## 🏷️ Attributed Graphs
*Graphs where nodes are accompanied by feature vectors (attributes).*

| Dataset | Type | # Nodes | # Edges | # Feat. | # Labels | Link |
|:---|:---:|:---|:---|:---|:---:|:---:|
| **Cora** | <span class="tag-directed">Dir</span> | 2,708 | 5,429 | 1,433 | 7 | [[raw]](https://linqs.soe.ucsc.edu/data) |
| **Citeseer** | <span class="tag-directed">Dir</span> | 3,327 | 4,732 | 3,703 | 6 | [[raw]](https://linqs.soe.ucsc.edu/data) |
| **Pubmed** | <span class="tag-directed">Dir</span> | 19,717 | 44,338 | 500 | 3 | [[raw]](https://linqs.soe.ucsc.edu/data) |
| **PPI** | <span class="tag-undirected">Undir</span> | 56,944 | 818,716 | 50 | 121 | [[raw]](https://snap.stanford.edu/graphsage/) |
| **Reddit** | <span class="tag-undirected">Undir</span> | <span class="highlight-num">232,965</span> | <span class="highlight-num">11.6M</span> | 602 | 41 | [[raw]](https://drive.google.com/drive/folders/1zycmmDES39zVlbVCYs88JTJ1Wm5FbfLz) |
| **Ogbn-ArXiv** | <span class="tag-undirected">Undir</span> | 169,343 | 1.15M | 128 | 40 | [[raw]](https://drive.google.com/drive/folders/1zycmmDES39zVlbVCYs88JTJ1Wm5FbfLz) |

### 🛠️ Usage Example
```python
from scipy import sparse
# Node attributes can be loaded as a sparse matrix
features = sparse.load_npz("attrs.npz")
print(f"Feature matrix shape: {features.shape}")
