# IIITH\_CV\_Internship\_2026

All my weekly tasks and final project shared here


# End-to-End Custom Object Detection Pipeline

\*\*Developed during the AI/ML Training Program at IIIT Hyderabad \& iHub-Data\*\*



\## 📌 Project Overview

This repository documents my week-by-week progression in building a complete Computer Vision pipeline. The project transitions from basic video frame manipulation to utilizing pre-trained YOLO models, and finally culminates in the end-to-end creation, annotation, and training of a custom object detection model.



\---



\## 🗓️ Weekly Development Log



\### Week 1: Data Manipulation \& Preprocessing

The foundational week focused on media processing and handling video data at the frame level using Linux command-line utilities.

\* \*\*Frame Extraction:\*\* Utilized `yt-dlp` to source raw video footage and `ffmpeg` to extract individual image frames from the stream.

\* \*\*Video Reconstruction:\*\* Generated a continuous image sequence at 30 frames per second (yielding \~1,800 images for a 1-minute clip) and reconstructed them back into a seamless video using `ffmpeg`.

\* \*\*Audio Engineering:\*\* Used Audacity to crop a royalty-free audio track to exactly 1-minute, merging it with the reconstructed video via `ffmpeg` to finalize the output.



\### Week 2: Environment Setup \& Pre-Trained Inference

This week introduced Python environment management and the implementation of out-of-the-box object detection models.

\* \*\*Environment Configuration:\*\* Established an isolated Python virtual environment (`venv`) to manage dependencies securely.

\* \*\*Ultralytics Integration:\*\* Installed the `ultralytics` package to interface with state-of-the-art YOLO architectures.

\* \*\*Object Detection:\*\* Deployed a pre-trained YOLO model to detect default classes within my custom video dataset.

\* \*\*Pipeline Integration:\*\* Extracted the newly annotated frames (containing bounding boxes), stitched them back into a video, added a synchronized audio track, and evaluated the pre-trained model's limitations.



\### Week 3: Semantic Segmentation \& Matrix Analysis

Transitioned from basic bounding boxes to pixel-perfect semantic segmentation and advanced video presentation.

\* \*\*Semantic Segmentation:\*\* Executed pixel-wise classification on the dataset to map the precise boundaries of objects, analyzing how this differs fundamentally from standard object detection.

\* \*\*Metrics Evaluation:\*\* Analyzed YOLO performance metrics generated in the `runs/detect/` directories to understand model accuracy.

\* \*\*Visual Stacking:\*\* Engineered a complex `ffmpeg` command utilizing the `vstack` filter to stack three synchronized videos vertically: the raw footage, the object-detected footage, and the semantically segmented footage, complete with a replaced audio track.



\### Week 4: Dataset Engineering \& Custom Annotation

Shifted focus from pre-trained models to the architecture of YOLO configuration files and the creation of a proprietary dataset.

\* \*\*Architecture Research:\*\* Authored a technical report breaking down YOLO metadata configurations, including `.yaml` files, class indexing, and bounding box coordinate mapping.

\* \*\*Custom Dataset Creation:\*\* Selected a fresh, real-world video and extracted frames at 10 fps to generate a raw dataset of 600 images.

\* \*\*Data Splitting:\*\* Architected a strict dataset split, allocating \~100 images for training, \~40 for validation (separated by time intervals to prevent data leakage), and reserving the rest for testing.

\* \*\*Manual Annotation:\*\* Deployed `label-studio` in an isolated environment to manually annotate the custom training and validation subsets, exporting the bounding boxes into strict YOLO `.txt` format.



\### Week 5: Model Forging, Training \& Inference

The final week focused on data optimization, training a custom neural network, and running inference on unseen data.

\* \*\*Data Optimization:\*\* Programmatically resized the training and validation images using `ffmpeg` (scaling width to 384px while preserving aspect ratio) to optimize GPU memory load during training.

\* \*\*Custom Model Training:\*\* Ignited the training sequence on a base YOLO model, utilizing a high number of epochs while actively monitoring training vs. validation loss to identify and prevent overfitting.

\* \*\*Weight Extraction:\*\* Successfully generated and saved a custom set of learned weights (`best.pt`) optimized specifically for my annotated classes.

\* \*\*Final Inference:\*\* Deployed the custom weights to run inference on the unseen test dataset. Stitched the resulting predictions into a final showcase video, demonstrating the real-world application of the newly trained custom object detector.



\---

\*\*Author:\*\* Anirudh Sai

\*\*Academics:\*\* BE in CSE (NGIT)

