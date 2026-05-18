# Object Detection Web App

## Overview

**Type:** Object Detection / Computer Vision Web App  
**Status:** Completed  
**GitHub:** https://github.com/pan-k15/object-detection-web

Object Detection Web App is a Streamlit-based web application for detecting objects in uploaded images. It uses YOLOv5 with the Ultralytics inference pipeline to process one or more images, display detection results, and show annotated output images with bounding boxes.

## Details

| Field | Information |
| --- | --- |
| Project name | Object Detection Web App |
| Project type | Object Detection / Computer Vision Web App |
| Main technology | Python, Streamlit, YOLOv5, Ultralytics, PyTorch, OpenCV, Pillow, Pandas |
| Model | YOLOv5s (`yolov5s.pt`) |
| Target runtime | Python 3.8+ |
| Repository | https://github.com/pan-k15/object-detection-web |

## Description

This project provides a browser-based interface for running object detection on uploaded images. Users can upload multiple PNG, JPG, or JPEG files, adjust the confidence threshold, and view detection results directly in the app.

The app resizes images to 640 by 640 before inference, runs YOLOv5 detection, saves annotated outputs to the `runs/detect/` folder, and reads those outputs back into the Streamlit interface. It also displays structured result tables with detected classes, bounding boxes, and confidence scores.

## Images

Recommended screenshots to add:

- `./images/upload-screen.png` - Streamlit image upload screen
- `./images/results-table.png` - Detection results table
- `./images/annotated-output.png` - YOLO bounding-box output
- `./images/confidence-slider.png` - Confidence threshold control

## Features

- Upload multiple images in one run
- Support PNG, JPG, and JPEG files
- Adjust detection confidence threshold with a Streamlit slider
- Run YOLOv5 object detection in the browser workflow
- Display per-image detection results as a DataFrame
- Show annotated output images with bounding boxes
- Resize images to 640 by 640 for consistent model input
- Reset saved detection outputs from the `runs/` directory

## Workflow

| Step | Description |
| --- | --- |
| 1 | Select a confidence threshold |
| 2 | Upload one or more images |
| 3 | Resize each image to 640 by 640 |
| 4 | Run YOLOv5 object detection |
| 5 | Display detected classes, bounding boxes, and confidence scores |
| 6 | Show annotated detection images |
| 7 | Reset generated outputs when needed |

## Project Structure

| File / Folder | Purpose |
| --- | --- |
| `app.py` | Main Streamlit application |
| `yolov5s.pt` | Pre-trained YOLOv5s model weights |
| `requirements.txt` | Python dependencies |
| `modules/load_model.py` | Detection class for loading YOLOv5 and running inference |
| `modules/get_image.py` | Helper for reading generated detection output images |

## Links

- **GitHub:** https://github.com/pan-k15/object-detection-web
- **Streamlit:** https://streamlit.io/
- **Ultralytics:** https://github.com/ultralytics/ultralytics
- **YOLOv5:** https://github.com/ultralytics/yolov5
- **PyTorch:** https://pytorch.org/

## Notes

The repository includes the `yolov5s.pt` weights, so the model does not need a separate manual download. Detection outputs are saved by YOLO under `runs/detect/`, then loaded back into the web app for display.
