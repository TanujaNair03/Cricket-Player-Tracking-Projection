# Cricket Player Tracking & Top-View Projection

## Installation & Setup
1. Open the provided Jupyter Notebook in Google Colab.
2. Ensure you have a GPU runtime enabled (Runtime > Change runtime type > T4 GPU).
3. Mount your Google Drive and ensure the project folder contains the source video and ground images.

## Dependencies
- python 3.10+
- ultralytics (YOLOv11)
- opencv-python
- numpy
- supervision
- scikit-learn

## Steps to Run
1. Run the **Setup** cell to install libraries and mount Drive.
2. (Optional) Run **Data Preparation** and **Training** if you wish to retrain the model.
3. Run the **Homography Calibration** cell to establish the pitch coordinates.
4. Run the **Final Submission** cell to generate the output video.

## Parameters
- Confidence Threshold: 0.15
- Max Frames: 900 (First 30 seconds)
- Tracker: ByteTrack
