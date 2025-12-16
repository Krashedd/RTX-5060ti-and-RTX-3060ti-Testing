# Evaluating Generational Improvements in NVIDIA x60-Class GPUs Under Academic AI Workloads

This repository contains the finalized paper, benchmarking data, and supporting materials for the study:

**“Evaluating Generational Improvements in NVIDIA x60-Class GPUs Under Academic AI Workloads”**

The study presents a controlled comparison between the **NVIDIA RTX 3060 Ti (Ampere)** and **NVIDIA RTX 5060 Ti (Blackwell)** using representative academic AI training workloads under identical system conditions and an enforced **8 GB VRAM constraint**.

Repository contents include the published paper and the complete benchmarking results used in the analysis.

---

## Repository Contents

- **Paper/**
  - `Evaluating_Generational_Improvements_in_NVIDIA_x60-Class_GPUs.pdf`
- **Results/**
  - `full_results.xlsx` – Raw benchmarking results and derived metrics

---

## Overview

Consumer-grade x60-class GPUs are widely used by students and academic researchers due to their balance of affordability and performance. This study evaluates whether upgrading within the same GPU tier provides meaningful benefits for real-world academic AI training workloads.

Four representative workloads were evaluated:

- **ResNet-152** – Image classification (Oxford-IIIT Pet)
- **DistilBERT** – NLP text classification (AG News 2K subset)
- **YOLOv8n** – Object detection (COCO 5K subset)
- **YOLOv8m** – Object detection (COCO 5K subset)

To ensure experimental fairness, the RTX 5060 Ti was constrained to the same VRAM capacity as the RTX 3060 Ti, isolating architectural and efficiency improvements from memory-driven advantages.

---

## Experimental Setup

- **CPU:** Intel Core i7-12700K  
- **Memory:** 32 GB DDR4 (ECC)  
- **Storage:** 2 × 1 TB WD Black SN850X (one per GPU environment)  
- **Operating System:** Windows 11  
- **Software Stack:**  
  - CUDA 12.9  
  - PyTorch  
  - Ultralytics (YOLOv8)  
  - Visual Studio Code  

Each GPU was tested in isolation using a dedicated NVMe drive and a clean software environment to avoid driver or library conflicts.

---

## Metrics Collected

The following metrics were recorded across all experiments:

- Training throughput  
- Total training time  
- Average and peak VRAM usage  
- GPU utilization  
- Average power draw  
- Performance per watt  
- Final validation accuracy / mAP  

These metrics enable a balanced evaluation of training speed, efficiency, and model correctness under academic workloads.

---

## Key Findings

- Performance differences between the RTX 3060 Ti and RTX 5060 Ti are modest for lighter workloads.
- The RTX 5060 Ti consistently demonstrates **substantially lower power consumption**, resulting in significantly improved performance-per-watt.
- For heavier workloads (YOLOv8m), the RTX 5060 Ti exhibits clearer performance advantages, highlighting the impact of architectural efficiency as model complexity increases.
- Older x60-class GPUs remain viable for basic academic training, while newer generations offer improved efficiency and scalability.

---

## Citation

If you use this repository for academic or benchmarking purposes, please cite:

**IEEE Style:**

C. J. C. Cangco, “GPU Benchmarking Code for Academic AI Workloads,” GitHub repository, 2025.  
[Online]. Available: https://github.com/Krashedd/GPU-AI-Training-Evaluation-RTX-5060ti-16GB-RX-9060XT-16GB-on-Windows

(Reference number to be updated in the final paper.)

---

## Notes

- This repository reflects **realistic academic workflows** using consumer-grade hardware.
- The enforced VRAM constraint ensures a fair generational comparison focused on architectural efficiency.
- Results are intended to guide students and researchers in making informed GPU upgrade decisions.

---

## Contact

**Cedric John C. Cangco**  
Mapúa University  
cccangco@mymail.mapua.edu.ph
