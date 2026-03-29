Motion Entropy-Driven Risk Assessment: A Real-Time Framework for Crowd Anomaly Detection from Surveillance Video
Official GitHub repository for the paper: "Motion Entropy-Driven Risk Assessment: A Real-Time Framework for Crowd Anomaly Detection from Surveillance Video".
Proposed System Diagram
<img width="871" height="611" alt="image" src="https://github.com/user-attachments/assets/6e077b3e-1762-453a-8892-c720d632e003" />

This research introduces a computationally efficient framework for real-time stampede risk assessment by integrating YOLOv8 for crowd localization, Farneback Optical Flow for motion analysis, and Shannon Entropy for quantifying crowd disorder.

Key Features
Hybrid Perception: Combines deep learning (YOLOv8) with statistical physics (Entropy).

Real-Time Performance: Achieves 30.3 FPS on standard hardware, suitable for immediate early warning systems.

Adaptive Thresholding: Dynamically adjusts to crowd density, lighting, and camera perspectives to minimize false alarms.

Granular Analysis: Grid-based spatial evaluation to detect localized panic before it spreads.
Methodology Overview
The framework operates in four major stages:

Crowd Localization: YOLOv8 generates binary person masks, refined with Gaussian smoothing.

Motion Extraction: Dense motion fields are computed using optimized Farneback Optical Flow.

Disorder Quantification: Shannon entropy measures directional randomness in crowd movement.

Risk Classification: Regions are classified into Normal, High-Risk, or Stampede-Prone using adaptive thresholds.

(Note: Use this to explain the YOLOv8 backbone)

Visual Results
The system provides real-time color-coded alerts:

🔵 Blue: Normal coordinated flow.

🟡 Orange: High-risk / Early warning signs of instability.

🔴 Red: Stampede-prone / Critical panic detected.

Installation & Usage
Prerequisites
Bash
pip install ultralytics opencv-python numpy
Run the Framework
Clone the repository.

Update the video_path and model_path in the notebook.

Run the cells to see the Sequential Log Output and the live preview.

Repository Structure
Notebook/: Contains the .ipynb file with full implementation and sequential logs.

Weights/: Link to the trained YOLOv8 weights (refer to README for external link).

Results/: Screenshot of the frame analysis results and confusion matrix.

Citation
If you find this work useful for your research, please cite our paper:

Code snippet
@article{Thulasimani2026Stampede,
  title={Motion Entropy-Driven Risk Assessment: A Real-Time Framework for Crowd Anomaly Detection from Surveillance Video},
  author={Thulasimani, K. and Pooja, J. and Saveeth, R. and Kannadhasan, S.},
  journal={The Visual Computer},
  year={2026},
  publisher={Springer}
}
