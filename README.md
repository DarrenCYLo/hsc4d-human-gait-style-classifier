1.	HSC4D human gait style classifier
This repo contains a pipeline to:
•	extract 5 interpretable kinematic features from the HSC4D dataset
•	create weak style labels (fast/slow/dragging/sharp_turn) using train-only thresholds
•	train and evaluate a RF using LOSO
•	export results to CSV files

2.	Dataset The HSC4D dataset is not included in this repository and must be downloaded.
Download it from: Main site: http://www.lidarhumanmotion.net/data-hsc4d/
Google Drive folder: https://drive.google.com/drive/folders/1c6iGtqcAhPmzSsoep-WB-g_kJQjMZl-t
Download and extract these folders:
•	campus_road
•	climbing_gym
•	lab_building

3.	Folder location This code expects the extracted dataset folders to be in one of these locations:
Option 1 (recommended):
•	Downloads/campus_road/
•	Downloads/climbing_gym/
•	Downloads/lab_building/

Option 2:
•	Downloads/HSC4D/campus_road/
•	Downloads/HSC4D/climbing_gym/
•	Downloads/HSC4D/lab_building/

Inside each folder there should be a *_pos.csv file (campus_road_pos.csv).

4.	Requirements Run in Anaconda and JupyterLab.
Python packages used:
•	numpy, pandas, scipy
•	scikit-learn
•	matplotlib

5.	How to run Open JupyterLab and run the "pipeline" code and it will find *_pos.csv automatically It will compute the five kinematic features, labels and LOSO evaluation
Outputs will be created in:
•	outputs/hsc4d_clip_features.csv

Run the “results artefacts” code to export reports and predictions:
•	Saves to: outputs/results_exports/

Files created:
•	per_scene_class_counts_GLOBAL.csv
•	looo_reports_TRAINONLY.csv
•	looo_predictions_TRAINONLY.csv
•	looo_thresholds_TRAINONLY.csv

6.	Notes Please follow the dataset license and terms on the official site as the HSC4D dataset remains the property of Dai et al (2022).
