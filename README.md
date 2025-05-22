# Excitation-Inhibition Balance and Fronto-Limbic Connectivity Drive TMS Treatment Outcomes in Refractory Depression

This repository includes the code required to reproduce the results in: "Excitation-Inhibition Balance and Fronto-Limbic Connectivity Drive TMS Treatment Outcomes in Refractory Depression"

### Journal Information:
bioRxiv (2025)  
DOI: https://doi.org/10.1101/2025.04.23.648963

### Authors:
- Davide Momi¹'²'³
- Zheng Wang¹
- Mohammad P. Oveisi¹'⁴
- Kevin Kadak¹'⁵
- Sorenza P. Bastiaens¹'⁵
- Jennifer I. Lissemore²
- Yoshihiro Noda⁶'⁷
- Jonathan Downar⁸
- Fidel Vila Rodriguez⁹'¹⁰
- Rebecca Strafella¹¹
- Zafiris J Daskalakis¹²
- Christoph Zrenner¹¹
- Reza Zomorrodi¹¹
- Camarin E. Rolle²
- Manish Saggar²
- Nolan Williams²
- Corey J. Keller²'³'¹³
- Daniel M. Blumberger¹¹
- Daphne Voineskos¹¹
- John D. Griffiths¹'⁴'⁵'⁷

### Affiliations:
¹ Krembil Centre for Neuroinformatics, Centre for Addiction and Mental Health (CAMH), Toronto, Canada  
² Department of Psychiatry and Behavioral Sciences, Stanford University Medical Center, Stanford, CA, USA  
³ Wu Tsai Neurosciences Institute, Stanford University, Stanford, CA, USA  
⁴ Institute of Biomedical Engineering, University of Toronto, Toronto, Canada  
⁵ Institute of Medical Science, University of Toronto, Toronto, Canada  
⁶ Department of Neuropsychiatry, Keio University School of Medicine, Tokyo, Japan  
⁷ Department of Psychiatry, Mita Hospital, International University of Health and Welfare, Tokyo, Japan  
⁸ Department of Psychiatry, Temerty Faculty of Medicine, University of Toronto, Toronto, Ontario, Canada  
⁹ Non-Invasive Neurostimulation Therapies Laboratory, Department of Psychiatry, Faculty of Medicine, University of British Columbia, Vancouver, BC, Canada  
¹⁰ School of Biomedical Engineering, Faculty of Applied Science | Faculty of Medicine, University of British Columbia, Vancouver, BC, Canada  
¹¹ Temerty Centre for Therapeutic Brain Intervention, Campbell Family Mental Health Research Institute, Centre for Addiction and Mental Health, Toronto, Ontario, Canada  
¹² Department of Psychiatry, University of California San Diego, La Jolla, California  
¹³ Veterans Affairs Palo Alto Healthcare System, Palo Alto, CA, USA

#### Please read our paper, and if you use this code, please cite our paper:
bioRxiv (2025) - DOI: https://doi.org/10.1101/2025.04.23.648963

## Investigating neurophysiological mechanisms of iTBS efficacy in treatment-resistant depression through TMS-EEG and whole-brain modeling

This study combines longitudinal TMS-EEG measurements with whole-brain computational modeling to investigate the neurophysiological mechanisms underlying treatment response in treatment-resistant depression (TRD). Our integrated approach revealed two key findings: (1) successful iTBS treatment was characterized by specific reductions in low-frequency (3–10 Hz) oscillatory power, reflecting shifts in excitation-inhibition (E/I) balance toward greater inhibitory control, and (2) a pre-treatment brain state characterized by anti-phase dynamics between left DLPFC and subgenual anterior cingulate cortex (sgACC) predicted clinical outcomes.

![alt text](https://github.com/YourUsername/TMS_Depression_2025/blob/main/img/Figure_1.png)

## Methodological workflow for TMS-EEG data analysis and connectome-based neurophysiological modeling

(A) Single-pulse TMS-EEG evoked responses and HRSD-17 depression scale were recorded before and after 30 days' iTBS therapy in 90 patients with treatment-resistant depression. (B) Anatomical connectivity was derived from Human Connectome Project diffusion-weighted MRI tractography data. (C) The Jansen-Rit neural mass model was embedded in 200 cortical regions for simulating TMS-evoked responses. (D) Lead field matrices projected neural activity to EEG channel space. (E) Model parameters were optimized using ADAM algorithm with autodiff-computed gradients. (F) Fitted models were analyzed to identify neurophysiological signatures of treatment response.

![alt text](https://github.com/YourUsername/TMS_Depression_2025/blob/main/img/Figure_5.png)

## Data   

The data used in this study were collected from 90 participants as part of a triple-blind randomized controlled trial conducted at the Centre for Addiction and Mental Health, University Health Network, and the University of British Columbia (clinicaltrials.gov identifier NCT02729792). Participants underwent TMS-EEG assessments both at baseline and after iTBS treatment targeting the left dorsolateral prefrontal cortex (L-DLPFC). The iTBS protocol consisted of daily treatment for 6 weeks (30 sessions, 5 days/week) with 1200 total pulses delivered per day.

**Inclusion criteria:**
- Age 18-59 years
- Major depressive disorder diagnosis (Mini-International Neuropsychiatric Interview)
- Baseline HRSD-17 score ≥18 (moderate-to-severe depression)  
- Stable psychotropic medications for ≥4 weeks prior to screening
- Treatment resistance (failed to respond to ≥1 adequate antidepressant trial or unable to tolerate ≥2 different trials)

Structural MRI data for anatomical connectivity priors are from the Human Connectome Project dataset (Van Essen et al., 2012), consistent with previous modeling work (Momi et al. 2023).

## Key Findings

### 1. Enhanced inhibition in responders following iTBS
Responders showed significantly greater reduction in 3-10 Hz oscillatory power compared to non-responders, with computational modeling indicating this reflects shifts in E/I balance toward greater inhibitory control through reduced excitatory drive to cortical pyramidal cells.

### 2. Responder-specific elevated inhibition after iTBS treatment
Analysis of Jansen-Rit model parameters revealed significant increases in inhibitory-to-pyramidal (I→P) synaptic weights in responders only, with pre-treatment I→P weights negatively correlating with post-treatment depression severity scores (r = -0.56, p < 0.001).

### 3. Subgenual-prefrontal interaction predicts iTBS efficacy
Pre-treatment brain states characterized by anti-phase relationships between left DLPFC and sgACC predicted clinical outcomes, with responders showing significantly higher sgACC engagement patterns at baseline (p < 0.001).

### 4. Greater trajectory deviation and increased stability in neural dynamics
iTBS induced more substantial reconfiguration of brain state dynamics in responders, characterized by greater reorganization and increased attractor convergence, suggesting enhanced stability and reduced susceptibility to external perturbations.

## Notebooks

This repository contains Jupyter notebooks that replicate the code and results presented in our paper. Each notebook serves a specific purpose as described below:

| Notebook | Run | View | Description |
| - | --- | ---- | ----------- |
| TMS_EEG_Preprocessing | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YourUsername/TMS_Depression_2025/blob/main/code/TMS_EEG_Preprocessing.ipynb) | [![View the notebook](https://img.shields.io/badge/render-nbviewer-orange.svg)](https://nbviewer.jupyter.org/github/YourUsername/TMS_Depression_2025/blob/main/code/TMS_EEG_Preprocessing.ipynb?flush_cache=true) | This notebook demonstrates TMS-EEG data preprocessing and artifact removal procedures. |
| Spectral_Analysis | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YourUsername/TMS_Depression_2025/blob/main/code/Spectral_Analysis.ipynb) | [![View the notebook](https://img.shields.io/badge/render-nbviewer-orange.svg)](https://nbviewer.jupyter.org/github/YourUsername/TMS_Depression_2025/blob/main/code/Spectral_Analysis.ipynb?flush_cache=true) | This notebook replicates the time-frequency analysis of TMS-induced oscillatory power. |
| Whole_Brain_Modeling | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YourUsername/TMS_Depression_2025/blob/main/code/Whole_Brain_Modeling.ipynb) | [![View the notebook](https://img.shields.io/badge/render-nbviewer-orange.svg)](https://nbviewer.jupyter.org/github/YourUsername/TMS_Depression_2025/blob/main/code/Whole_Brain_Modeling.ipynb?flush_cache=true) | This notebook shows how to fit the Jansen-Rit neural mass model to individual TMS-EEG data. |
| Parameter_Analysis | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YourUsername/TMS_Depression_2025/blob/main/code/Parameter_Analysis.ipynb) | [![View the notebook](https://img.shields.io/badge/render-nbviewer-orange.svg)](https://nbviewer.jupyter.org/github/YourUsername/TMS_Depression_2025/blob/main/code/Parameter_Analysis.ipynb?flush_cache=true) | This notebook analyzes physiological model parameters and E/I balance differences between responders and non-responders. |
| Brain_State_Analysis | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YourUsername/TMS_Depression_2025/blob/main/code/Brain_State_Analysis.ipynb) | [![View the notebook](https://img.shields.io/badge/render-nbviewer-orange.svg)](https://nbviewer.jupyter.org/github/YourUsername/TMS_Depression_2025/blob/main/code/Brain_State_Analysis.ipynb?flush_cache=true) | This notebook replicates the PLS analysis identifying treatment-predictive brain states. |
| Neural_Trajectory_Analysis | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YourUsername/TMS_Depression_2025/blob/main/code/Neural_Trajectory_Analysis.ipynb) | [![View the notebook](https://img.shields.io/badge/render-nbviewer-orange.svg)](https://nbviewer.jupyter.org/github/YourUsername/TMS_Depression_2025/blob/main/code/Neural_Trajectory_Analysis.ipynb?flush_cache=true) | This notebook shows the neural trajectory analysis in model-derived state space. |

## References

- Blumberger, D. M. et al. A randomized sham controlled comparison of once vs twice-daily intermittent theta burst stimulation in depression: A Canadian rTMS treatment and biomarker network in depression (CARTBIND) study. Brain Stimulat. 14, 1447–1455 (2021).
- Gramfort, A. et al. MNE software for processing MEG and EEG data. NeuroImage 86, 446–460 (2014).
- Jansen, B. H. & Rit, V. G. Electroencephalogram and visual evoked potential generation in a mathematical model of coupled cortical columns. Biol. Cybern. 73, 357–366 (1995).
- Kingma, D. P. & Ba, J. Adam: A Method for Stochastic Optimization. arXiv preprint arXiv:1412.6980 (2017).
- Momi, D., Wang, Z. & Griffiths, J. D. TMS-evoked responses are driven by recurrent large-scale network dynamics. eLife 12, e83232 (2023).
- Schaefer, A. et al. Local-Global Parcellation of the Human Cerebral Cortex from Intrinsic Functional Connectivity MRI. Cereb. Cortex 28, 3095–3114 (2018).
- Strafella, R. et al. Identifying Neurophysiological Markers of Intermittent Theta Burst Stimulation in Treatment-Resistant Depression Using Transcranial Magnetic Stimulation–Electroencephalography. Biol. Psychiatry 94, 454–465 (2023).
- Van Essen, D. C. et al. The Human Connectome Project: a data acquisition perspective. NeuroImage 62, 2222–2231 (2012).
