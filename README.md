# General-Compositional-Data-Analysis
This ensures the quality of rows and columns required for general compositional data analysis.

# ITAGAKI-SYSTEM: Ultimate Cross-Sectional Profiler (V2026.4.27)

A robust computational framework for microbiome and compositional data analysis, focusing on **Physical Reliability Mapping** and **System Stability Tracking**.

## 🧬 Overview

Traditional microbiome analysis often fails to distinguish between biological signals and physical noise. The **ITAGAKI-SYSTEM** addresses this by implementing "10x Noise Floor" logic, ensuring that only physically reliable taxa are used for quantitative conclusions.

### Key Features
- **Strict Reliability Profiling:** Individual-based noise floor calculation (1/Effective Library Size).
- **Physical Reliability Heatmap:** Visualization of reliable, uncertain, and absent taxa with fixed sample integrity.
- **Universal Reliable Taxa (URT) Extraction:** Automated filtering for high-confidence core microbiomes.
- **LOO-Stability Tracker:** Leave-One-Out analysis using the **Invariance Ratio (IR)** to identify "System Perturbers" (outliers based on physical integrity) or sampling miss.

## 📚 Academic Citation

If you use this software or its logic in your research, please cite the following works:

1. **Pearson, K. (1897).**  DOI: [10.1098/rspl.1896.0076](https://doi.org/10.1098/rspl.1896.0076)
2. **Ohta, T.    (2011).**  DOI: [10.1007/s11004-011-9332-y](https://doi.org/10.1007/s11004-011-9332-y)
3. **Itagaki, T. (2024).**  DOI: [10.3390/microorganisms12071484](https://doi.org/10.3390/microorganisms12071484)
4. **Itagaki, T. (2026).**  DOI: [10.13140/RG.2.2.35655.05287](https://doi.org/10.13140/RG.2.2.35655.05287)
## 🚀 Getting Started

### Prerequisites
- R (version 4.0.0 or higher)
- A dataset where rows = Samples and columns = Taxa (Relative Abundance).

### Implementation Logic
The system evaluates each taxon based on the following physical criteria:
- **Reliable:** Non-zero and $\ge 10 \times$ Noise Floor.
- **Uncertain (Presence):** Detected, but $< 10 \times$ Noise Floor.
- **Undetected:** Absolute zero.

## 📊 Outputs

The system generates several diagnostic reports:
- `ITAGAKI_Strict_Individual_Reliability_Report.pdf`: Detailed log-scale plots for every sample.
- `Reliability_Heatmap_RowFixed.pdf`: A comprehensive map of data certainty across the entire cohort.
- `Stability_Perturbation_Report.pdf`: Identification of samples that destabilize the physical integrity of the system.
- `Universal_Reliable_Taxa_ZeroFree.csv`: A cleaned, high-confidence matrix ready for downstream statistical analysis (e.g., identification of invariant components, ALR transformation).

## ⚖️ License

This project is licensed under the MIT License - see the [LICENSE](https://opensource.org) page for details.

---
**Developed by:** Tatsuki Itagaki (2026)  
*Reliability is the shortest path to truth.*
*For information on how to identify invariant components, please refer to another repository.*
