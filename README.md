# Acoustic Waveform Signal Recovery 🎵📈

This repository contains a Jupyter Notebook (`music.ipynb`) that focuses on analyzing and visualizing highly sparse acoustic waveform datasets. The notebook specifically explores how to differentiate between known signal contexts and hidden ground truth targets within the audio data.

## 📝 Overview

In many signal processing scenarios, audio datasets might be corrupted, incomplete, or heavily sparse. This project visualizes acoustic waveforms to study the underlying physics of the audio signals by separating intact "context" points from missing "target" points.

The notebook processes a dataset containing **8,000,000 rows** of spectral audio data, where an overwhelming **80.00% of the signal is missing** (target points). 

## 📊 Dataset

The project relies on a CSV dataset (e.g., `spectral_graffiti_headley_recovered.csv`). The dataset contains the following key columns:
* `Sample_ID`: The unique identifier for a specific audio sample.
* `Time_ms`: The time step of the acoustic signal in milliseconds.
* `Value`: The normalized voltage amplitude of the acoustic waveform.
* `Is_Context`: A binary indicator representing the sparsity of the data:
  * `1` = Known Context (Intact data points)
  * `0` = Hidden Targets (Missing/Masked signal)

> **Note:** If you are running this locally, you will need to update the `file_path` variable in the notebook to point to your local copy of the dataset.

## 🚀 Features

* **Sparsity Checking**: Automatically calculates and outputs the sparsity of the dataset (percentage of missing signals).
* **Advanced Visualization**: Includes a robust plotting function (`plot_audio_sample`) that reconstructs the audio wave by:
  * Plotting known context points in **blue**.
  * Plotting hidden ground-truth target points in **red crosses**.
  * Drawing a faint line connecting the underlying true wave to demonstrate the signal's physics.
* **Random Sampling**: Randomly selects and plots audio samples from the dataset to compare differing acoustic structures.


