# mcPHASES Example Analysis

This repository provides an example notebook and script for working with the mcPHASES (**m**enstrual **c**ycle **P**hysiological, **H**ormonal, **a**nd **S**elf-**R**eported **E**vents and **S**ymptoms) dataset.

## Dataset Overview

mcPHASES represents a unique collection of multimodal physiological, hormonal, and self-reported data from 42 Canadian young adults who menstruate over the course of two 3-month periods. This dataset addresses critical gaps in existing research by providing comprehensive physiological and subjective data throughout complete menstrual cycles, allowing researchers to challenge conventional approaches that rely solely on self-reported information for menstrual health tracking and understanding.

### Data Collection

Study participants used multiple approaches to collect and record data:
- **Fitbit Sense Smartwatch** for continuous physiological monitoring
- **Dexcom G6 Continuous Glucose Monitor** for metabolic tracking
- **Mira Plus Starter Kit** for hormone level measurement
- **Daily Self-Report Diary** of symptoms, sleep quality, and stress levels

### Dataset Structure

The dataset is organized into 23 structured tables linked by participant identifier (`id`) and timeline variable (`day_in_study`). Data includes:

- **Demographic Information**: Age, education, employment, age at menarche
- **Self-Report and Hormone Data**: Daily symptoms, mood, menstrual flow, and hormone levels (LH, E3G, PdG)
- **Glucose Monitoring**: High-frequency continuous glucose data
- **Fitbit Metrics** (20 tables): Heart rate, activity, sleep stages, respiratory rate, temperature, VO₂ max, oxygen variation, and stress scores

**Data Access**: The complete dataset is hosted at [PhysioNet](https://physionet.org/content/mcphases/1.0.0/).

## Example Scripts

This repository provides two versions of the same analysis pipeline to help researchers get started with the mcPHASES dataset:

### 1. Jupyter Notebook (`mcphases_sample_analysis.ipynb`)
Interactive notebook demonstrating basic data exploration with step-by-step examples and visualizations.

### 2. Python Script (`mcphases_sample_analysis.py`)
Standalone Python version of the notebook examples, suitable for reference or integration into other projects.

Both examples include the following basic operations:
- **Data Import**: Loading and structuring a subset of mcPHASES CSV files: `hormones_and_selfreport.csv`, `resting_heart_rate.csv`, `computed_temperature.csv`
- **Cycle Detection and Labeling**: Identifying complete menstrual cycles from the data
- **Wearable Data Integration**: Combining physiological signals (heart rate, temperature) with hormone data (luteinizing hormone, estrogen, and progesterone) for comparative analysis

The scripts generate the following plots:
1. **Hormone Profiles**: Daily hormone levels across normalized menstrual cycles with confidence intervals
2. **Physiological Comparisons**: Boxplots comparing heart rate and temperature across cycle phases  
3. **Data Overview**: Cycle counts and basic dataset statistics

## Research Applications

The mcPHASES dataset enables investigations on several topics:

- **Cycle Variability Characterization**: Analyze inter- and intra-personal differences in cycle length, phase duration, and symptom patterns along with the influence of lifestyle factors like stress, sleep, and physical activity.
- **Physiological Variation Across Menstrual Phases**: Explore relationships between continuous physiological monitoring and hormone-defined cycle phases.
- **Predictive Model Development**: Leverage hormone-verified ground-truth labels to train machine learning algorithms for accurate prediction of ovulation, fertile windows, and symptom onset.

## Getting Started

1. Download the mcPHASES dataset from [PhysioNet](https://physionet.org/content/mcphases/1.0.0/)
2. Place the required CSV files in your working directory
3. Run the example scripts to see basic analysis patterns:
   - For interactive exploration: Open `mcphases_analysis.ipynb` in Jupyter Notebook / Google Colab
   - For a Python script: View `mcphases_analysis.py`
     
## Citation

If you use the mcPHASES dataset in your research, please cite the original dataset publication available on [PhysioNet](https://physionet.org/content/mcphases/1.0.0/):

**Lin, B., Li, J. Y., Kalani, K., Truong, K., & Mariakakis, A. (2025). mcPHASES: A Dataset of Physiological, Hormonal, and Self-reported Events and Symptoms for Menstrual Health Tracking with Wearables (version 1.0.0). PhysioNet. RRID:SCR_007345. https://doi.org/10.13026/zx6a-2c81**

## Related Work

The papers below offer additional perspectives on the two studies, including participants’ experiences with data collection, how those experiences influenced their sensemaking, and analyses of the collected data. Please note that the analyses below are based on all participants’ data. However, only a subset consented to data sharing for the mcPHASES dataset, therefore, results derived from the mcPHASES dataset may differ.

**Lin, G., Le, M. N., Truong, K. N., & Mariakakis, A. (2025). The Cognitive Strategies Behind Multimodal Health Sensemaking: A Menstrual Health Tracking Case Study. Proceedings of the ACM on Interactive, Mobile, Wearable and Ubiquitous Technologies, 9(3), 1-27.**

**Lin, G., Li, B., Li, J. Y., Zhao, C., Truong, K., & Mariakakis, A. (2024). Users' Perspectives on Multimodal Menstrual Tracking Using Consumer Health Devices. Proceedings of the ACM on Interactive, Mobile, Wearable and Ubiquitous Technologies, 8(3), 1-24.**

**Lin, G., Li, J. Y., Christofferson, K., Patel, S. N., Truong, K. N., & Mariakakis, A. (2024). Understanding wrist skin temperature changes to hormone variations across the menstrual cycle. npj Women's Health, 2(1), 35.**

**Lin, G., Siddiqui, R., Lin, Z., Blodgett, J. M., Patel, S. N., Truong, K. N., & Mariakakis, A. (2023). Blood glucose variance measured by continuous glucose monitors across the menstrual cycle. npj Digital Medicine, 6(1), 140.**
