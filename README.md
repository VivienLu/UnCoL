# Harmonizing Generalization and Specialization: Uncertainty-Informed Collaborative Learning for Semi-supervised Medical Image Segmentation

[![arXiv](https://img.shields.io/badge/IEEETMI-2026-blue)](https://arxiv.org/pdf/2512.13101)

Official PyTorch implementation of UnCoL from the paper: "Harmonizing Generalization and Specialization: Uncertainty-Informed Collaborative Learning for Semi-supervised Medical Image Segmentation" Accepted by IEEE Transactions on Medical Imaging (TMI), 2026.

## Contents

- [Abstract](#abstract)
- [Datasets](#datasets)
- [Usage](#usage)
- [Acknowledgment](#acknowledgment)

## Abstract

![avatar](./images/framework.jpg)

Vision foundation models have demonstrated strong generalization in medical image segmentation by leveraging large-scale, heterogeneous pretraining. However, they often struggle to generalize to specialized clinical tasks under limited annotations or rare pathological variations, due to a mismatch between general priors and task-specific requirements. To address this, we propose Uncertainty-informed Collaborative Learning (UnCoL), a dual-teacher framework that harmonizes generalization and specialization in semi-supervised medical image segmentation. Specifically, UnCoL distills both visual and semantic representations from a frozen foundation model to transfer general knowledge, while concurrently maintaining a progressively adapting teacher to capture fine-grained and task-specific representations. To balance guidance from both teachers, pseudo-label learning in UnCoL is adaptively regulated by predictive uncertainty, which selectively suppresses unreliable supervision and stabilizes learning in ambiguous regions. Experiments on diverse 2D and 3D benchmarks show that UnCoL achieves strong and competitive performance across metrics compared with existing semi-supervised methods and foundation model baselines. Moreover, our model delivers near fully supervised performance with markedly reduced annotation requirements.

## Datasets

**Dataset licensing term**:

* Pancreas dataset: https://wiki.cancerimagingarchive.net/display/Public/Pancreas-CT
* Type B Aorta Dissection dataset: https://github.com/XiaoweiXu/Dataset_Type-B-Aortic-Dissection     
* OASIS dataset: https://sites.wustl.edu/oasisbrains/

## Usage

1. Clone the repo.;

   ```
   git clone
   ```

2. Train or test the model;

   ```
   cd ./UnCoL/codes
   
   # 2D
   sh train2D.sh # Stage 1 / Stage 2 / Inference
   
   # 3D
   sh train3D.sh # Stage 1 / Stage 2 / Inference
   ```

## Acknowledgment

Part of the code is adapted from the open-source codebase and original implementations of algorithms, we thank these authors for their fantastic and efficient codebase:

*  SSL4MIS: https://github.com/HiLab-git/SSL4MIS
*  UPCoL: https://github.com/VivienLu/UPCoL
*  MedSAM: https://github.com/bowang-lab/MedSAM
*  SAM-Med3D: https://github.com/uni-medical/SAM-Med3D
