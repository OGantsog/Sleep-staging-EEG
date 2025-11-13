# Sleep EEG Analysis Project

## Overview

This repository contains code and resources for analyzing **sleep EEG data** using signal processing and machine learning techniques. The primary goal is to explore neural activity during different sleep stages, detect sleep-related events, and build tools for visualization and classification.

## Objectives

*   **Preprocessing**: Clean and filter raw EEG signals to remove artifacts and noise.
*   **Feature Extraction**: Compute features such as power spectral density, band power (delta, theta, alpha, beta), and event-related potentials.
*   **Sleep Stage Classification**: Implement algorithms to classify sleep stages (e.g., NREM, REM) based on EEG patterns.
*   **Event Detection**: Identify sleep phenomena such as spindles, K-complexes, and micro-arousals.
*   **Visualization**: Generate plots and spectrograms to illustrate EEG dynamics across sleep cycles.

***

## Dataset Details

This project uses the **Sleep-EDF Expanded dataset** from PhysioNet ( https://physionet.org/content/sleep-edfx/1.0.0/#files-panel ), which includes overnight polysomnographic recordings. Each recording contains multiple physiological signals:

### Channel Descriptions

| **Channel**        | **Type**    | **Location / Signal**    | **Role in Sleep Analysis**                                                                 |
| ------------------ | ----------- | ------------------------ | ------------------------------------------------------------------------------------------ |
| **EEG Fpz-Cz**     | EEG         | Frontopolar → Central    | Captures frontal and central brain activity; useful for detecting slow waves and spindles. |
| **EEG Pz-Oz**      | EEG         | Parietal → Occipital     | Records parietal and occipital activity; monitors alpha rhythms and visual cortex changes. |
| **EOG Horizontal** | EOG         | Eye movements            | Detects rapid eye movements; critical for identifying REM sleep and wakefulness.           |
| **Resp Oro-Nasal** | Respiratory | Mouth & nose airflow     | Tracks breathing patterns; helps detect apnea and respiratory irregularities.              |
| **EMG Submental**  | EMG         | Chin muscles             | Measures muscle tone; low tone indicates REM sleep, high tone suggests wake/NREM.          |
| **Temp Rectal**    | Temperature | Core body temperature    | Monitors circadian rhythm; temperature typically drops during sleep.                       |
| **Event Marker**   | Annotation  | Manual/automated markers | Stores events like lights off/on, arousals, or experimental conditions.                    |

***

## Tools & Libraries

*   **Python**: Core programming language
*   **MNE-Python**: EEG data handling and visualization
*   **NumPy / SciPy**: Signal processing and numerical computations
*   **Matplotlib / Seaborn**: Data visualization
*   **Scikit-learn**: Machine learning for classification tasks

***

## Project Structure

    ├── data/                # EEG datasets (not included in repo)
    ├── notebooks/           # Jupyter notebooks for analysis
    ├── src/                 # Python scripts for preprocessing and modeling
    ├── results/             # Output figures and metrics
    └── README.md            # Project documentation

***

## How to Use

1.  Clone the repository:
    ```bash
    git clone https://github.com/your-username/sleep-eeg-analysis.git
    ```
2.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3.  Run preprocessing and analysis scripts from `src/` or explore notebooks in `notebooks/`.

***

## Future Work

*   Advanced deep learning models for sleep stage classification
*   Integration with wearable EEG devices
*   Real-time signal processing pipeline