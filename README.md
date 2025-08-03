# K4: Online Log Anomaly Detection via Unsupervised Typicality Learning

**Authors**: Weicong Chen*, Vikash Singh*, Zahra Rahmani, Debargha Ganguly, Mohsen Hariri, Vipin Chaudhary  
**Affiliation**: Case Western Reserve University  
📄 [Read the paper on arXiv](https://arxiv.org/abs/2507.20051)

## Abstract

Log anomaly detection (LogAD) is crucial for identifying failures and threats in large-scale computing and cyberinfrastructure systems. However, most existing LogAD approaches suffer from key limitations: they depend on slow and error-prone log parsing, employ tightly coupled end-to-end pipelines, often require supervision for improved detection performance, and rely on flawed single-pass evaluation protocols that fail to reflect the temporal dynamics of real-world online detection. These issues significantly hinder scalability, adaptability, and the practical deployment of solutions.

To address these limitations, we introduce K4 (Knowing the Unknown by Knowing only the Known), a fully unsupervised, parser-independent, and representation-agnostic LogAD framework designed for high-performance online detection. At its core, K4 is grounded in a novel formulation based on representation-level typicality estimation, which transforms arbitrary log embeddings into compact and interpretable four-dimensional descriptors: Precision, Recall, Density, and Coverage (PRDC), which are swiftly computed via GPU-acceleration into geometric k-nearest neighbor statistics.

These descriptors inform lightweight, modular detectors, including KDE, GMM, OCSVM, and a new adaptation of DeepSVDD, which enables efficient and accurate anomaly scoring without relying on structured formats or log representation retraining.

To support realistic deployment scenarios, we also propose a principled chunk-based evaluation protocol that mimics online log ingestion, alleviates the performance overestimation and dataset undercoverage issues of prior single-pass evaluations, and enables reproducible benchmarking across datasets with varying anomaly densities.

Using this setup, we conduct over 125,000 experiments across three real-world datasets (HDFS, BGL, Thunderbird), six pre-trained embedding models, four detectors, and multiple training and log sampling configurations. Compared to six representative baseline methods spanning supervised, semi-supervised, self-supervised, and unsupervised paradigms, K4 consistently sets new state-of-the-art results (AUROC: 0.995–0.999, F1: 0.989–0.992) and outperforms all baselines by large margins—while keeping detector training under 4 seconds and per-sample inference latency as low as 4 µs, which are orders of magnitude faster than the most competitive alternatives.

## Citation

Please cite our paper using the following BibTeX entry:

```bibtex
@article{chen2025k4,
  title={K4: Online Log Anomaly Detection Via Unsupervised Typicality Learning},
  author={Chen, Weicong and Singh, Vikash and Rahmani, Zahra and Ganguly, Debargha and Hariri, Mohsen and Chaudhary, Vipin},
  journal={arXiv preprint arXiv:2507.20051},
  year={2025}
}
