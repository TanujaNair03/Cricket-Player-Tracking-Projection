# Cricket Player Tracking & Top-View Projection

## 💿 Installation Instructions
1. Clone this repository or download the project files.
2. Open the `.ipynb` notebook in **Google Colab**.
3. Mount your Google Drive when prompted to access the dataset and model weights.
4. Ensure the file structure in your Drive matches the paths defined in the "Configuration" section of the notebook.

## 📦 Required Dependencies
The following libraries are required to run the pipeline:
- `ultralytics` (YOLOv11)
- `opencv-python`
- `numpy`
- `supervision`
- `scikit-learn`
- `matplotlib`

You can install them all at once using:
`pip install ultralytics supervision opencv-python numpy scikit-learn`

## 🚀 Steps to Run the Complete Pipeline
1. **Setup:** Run the first cell to import libraries and mount Google Drive.
2. **Data Prep (Optional):** Run the Data Cleaning block if you wish to see how the raw labels were filtered.
3. **Calibration:** Execute the Homography Calibration cell. This establishes the 4-point mapping between the Video pitch and the Ground Map.
4. **Inference:** Run the Final Submission block. This loads the `best.pt` weights, processes the video, and generates the side-by-side tracking visualization.

## ⚙️ Configuration & Parameter Details
- **Weights Path:** Located in `weights/best.pt`.
- **Confidence Threshold:** `0.15` (Selected to minimize false positives from shadows).
- **Tracking:** `ByteTrack` algorithm with a 30-frame patience buffer.
- **Inference Size:** `imgsz=1280` (High resolution to detect distant fielders).
- **Field Boundary:** A 7-point polygon mask used to exclude spectators from tracking.
