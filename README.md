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
<img width="640" height="360" alt="image" src="https://github.com/user-attachments/assets/0713cc06-c33c-4b4d-9b4d-e5412123bae5" />





🟡 Orange: High-risk / Early warning signs of instability.
<img width="640" height="360" alt="image" src="https://github.com/user-attachments/assets/48a5e90b-afec-451b-96d2-d750e97c407c" />





🔴 Red: Stampede-prone / Critical panic detected.
<img width="640" height="360" alt="image" src="https://github.com/user-attachments/assets/e1f8ec0d-af31-43f4-a198-bd9bfc21d836" />





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
<img width="1083" height="484" alt="image" src="https://github.com/user-attachments/assets/3250b3c3-024b-4f99-b5fa-e4e65a7f07c7" />


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
