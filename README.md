# HR-OOV-SNOMED-CT

Hierarchical Retrieval with Out-Of-Vocabulary1 Queries: A Case Study on SNOMED CT

## Experiments

See [notebooks](/notebooks/) for code and experimental results.

## Data

Original OET data can be found at [zenodo.org](https://zenodo.org/records/10432003) **(ensure version 4 is selected)**.

Transformed OET datasets are provided under the [data directory](/data). Preprocessing scripts can be found alongside the provided notebooks.

## Models

Configurations for re-training models are available [here](./docs/retraining-models.md)

See the included [libraries] for re-training procedures.

These include [sentence-transformers](https://github.com/huggingface/sentence-transformers), [hierarchy transformers](https://github.com/KRR-Oxford/HierarchyTransformers), and [OnT](https://github.com/HuiYang1997/OnT).

Models will be published to HF (shortly).

## Environment

- OS: Ubuntu 24.04.4 LTS
- Python: 3.12
- CUDA VERSION: 13.1

## Hardware

- CPU: AMD 9965wx 24c/48t
- RAM: 768GB DDR5 5600MTs (JEDEC) ECC RDIMM
- GPU: RTX PRO 6000 Blackwell Max-Q

