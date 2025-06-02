# Heart-Rate-variability-analysis-using-MATLAB
This project analyzes an ECG (Electrocardiogram) signal to extract critical features such as R-peaks, heart rate variability (HRV) metrics, rhythm disturbances, and frequency-domain characteristics using MATLAB.

# Objective
The aim is to process raw ECG data to:

Remove noise and artifacts,

Detect R-peaks,

Calculate HRV metrics (RMSSD, SDNN),

Analyze rhythm disturbances,

Compute Power Spectral Density (PSD),

Visualize normalized ECG signals.

# Methodology
1. Data Acquisition
ECG signal is read from 100.dat using fread.

Sampling frequency: 360 Hz.

2. Preprocessing
Low-pass Butterworth filter to remove high-frequency noise.

High-pass Butterworth filter to eliminate low-frequency drift.

3. R-Peak Detection
Uses findpeaks() to locate R-waves.

From R-peak intervals, NN intervals are calculated.

4. HRV Metrics
RMSSD: Measures short-term variation (parasympathetic activity).

SDNN: Reflects overall HRV (sympathetic + parasympathetic).

5. Heart Rate Analysis
Heart rate (BPM) is calculated from average NN interval.

Visualized as a time series.

6. Rhythm Disturbance Detection
Compares RMSSD and SDNN against healthy thresholds.

Alerts if disturbance is suspected.

7. Frequency Domain Analysis
Uses Welch’s method to plot PSD.

Highlights frequency components of the ECG signal.

8. Normalization
ECG signal is normalized to the range [-1, 1] for standardization.

# Sample Results
Heart Rate: ~50 BPM

RMSSD: 9.3

SDNN: 7

Rhythm Status: Rhythm disturbance detected (below healthy range)
