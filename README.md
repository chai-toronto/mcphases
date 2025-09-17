# mcPHASES Dataset Analysis

This repository provides an example analysis script and notebook to get started with the mcPHASES (menstrual cycle Physiological, Hormonal, and Self-Reported Events and Symptoms) dataset, demonstrating basic data import, cycle labeling, and visualization techniques.

## Dataset Overview

The mcPHASES dataset represents a unique collection of multimodal physiological, hormonal, and self-reported data from 42 Canadian young adults who menstruate collected across two 3-month periods. This dataset addresses critical gaps in existing research by providing comprehensive physiological and subjective data throughout complete menstrual cycles, thereby challenging conventional calendar-based only approaches to menstrual health tracking and understanding.

### Data Collection

Participants used multiple monitoring devices and methods:
- **Fitbit Sense smartwatches** for continuous physiological monitoring
- **Dexcom G6 continuous glucose monitors** for metabolic tracking
- **Mira Plus Starter Kits** for hormone level measurement
- **Daily self-reports** of symptoms, sleep quality, and stress levels

### Dataset Structure

The dataset is organized into 23 structured tables linked by participant identifier (`id`) and timeline variable (`day_in_study`). Data includes:

- **Demographic information**: Age, education, employment, age at menarche
- **Self-report and hormone data**: Daily symptoms, mood, menstrual flow, and hormone levels (LH, E3G, PdG)
- **Glucose monitoring**: High-frequency continuous glucose data
- **Fitbit-derived metrics** (20 tables): Heart rate, activity, sleep stages, respiratory rate, temperature, VO₂ max, oxygen variation, and stress scores

**Data Access**: The complete dataset is hosted at [PhysioNet](https://physionet.org/content/mcphases/1.0.0/).

## Example Scripts

This repository provides two versions of the same example analysis to help researchers get started with the mcPHASES dataset:

### 1. Jupyter Notebook (`mcphases_sample_analysis.ipynb`)
Interactive notebook demonstrating basic data exploration with step-by-step examples and visualizations.

### 2. Python Script (`mcphases_sample_analysis.py`)
Standalone Python version of the notebook examples, suitable for reference or integration into other projects.

Both examples demonstrate:

#### Basic Operations
- **Data Import**: Loading and structuring mcPHASES CSV files
- **Cycle Detection and Labeling**: Identifying complete menstrual cycles from the data
- **Hormone Data Visualization**: Creating normalized plots of LH, estrogen (E3G), and progesterone (PdG) levels across cycle phases
- **Wearable Data Integration**: Combining physiological signals (heart rate, temperature) with hormone data for comparative analysis

#### Required Data Files
The analysis requires the following CSV files from the mcPHASES dataset:
- `hormones_and_selfreport.csv`
- `resting_heart_rate.csv`
- `computed_temperature.csv`

#### Example Visualizations
The scripts generate basic plots including:
1. **Hormone Profiles**: Daily hormone levels across normalized menstrual cycles with confidence intervals
2. **Physiological Comparisons**: Boxplots comparing heart rate and temperature across cycle phases  
3. **Data Overview**: Cycle counts and basic dataset statistics

## Research Applications

The mcPHASES dataset enables research across multiple domains:

**Biosensor-Menstrual Phase Mapping**: Investigate relationships between continuous physiological monitoring (temperature, heart rate variability, glucose) and hormone-defined cycle phases to develop non-invasive fertility tracking methods.

**Cycle Variability Characterization**: Analyze inter- and intra-individual differences in cycle length, phase duration, and symptom patterns, including the influence of lifestyle factors like stress, sleep, and physical activity.

**Hormone-Physiology Integration**: Examine how hormonal fluctuations throughout the menstrual cycle affect broader physiological systems through joint modeling of endocrine and sensor data.

**Predictive Model Development**: Leverage hormone-verified ground truth labels to train machine learning algorithms for accurate prediction of ovulation, fertile windows, and symptom onset, surpassing traditional calendar-based methods.

## Getting Started

1. Download the mcPHASES dataset from [PhysioNet](https://physionet.org/content/mcphases/1.0.0/)
2. Place the required CSV files in your working directory
3. Run the example scripts to see basic analysis patterns:
   - For interactive exploration: Open `mcphases_analysis.ipynb` in Jupyter Notebooks/ Google Colab
   - For reference code: View `mcphases_analysis.py`
     
## Citation

If you use the mcPHASES dataset in your research, please cite the original dataset publication available on PhysioNet. 

**Lin, B., Li, J. Y., Kalani, K., Truong, K., & Mariakakis, A. (2025). mcPHASES: A Dataset of Physiological, Hormonal, and Self-reported Events and Symptoms for Menstrual Health Tracking with Wearables (version 1.0.0). PhysioNet. RRID:SCR_007345. https://doi.org/10.13026/zx6a-2c81**
