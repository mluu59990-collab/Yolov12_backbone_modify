# YOLOv12 Backbone Modification for Improved Object Detection Accuracy

This repository presents a modified YOLOv12 backbone designed to improve object detection performance by integrating lightweight attention modules into the baseline architecture. The goal of this work is to achieve a better balance between detection accuracy and computational efficiency.

## Overview

The project focuses on improving the baseline YOLOv12s model through backbone redesign and module-level experimentation. Different lightweight attention and feature extraction blocks were evaluated to enhance feature representation while keeping the model practical for deployment.

The final modified model improved detection performance over the baseline YOLOv12s and also showed competitive results against YOLOv10s and YOLOv11s.

## Key Result

The proposed attention-enhanced YOLOv12 variant improved:

- **mAP@0.5:0.95** from **0.350** to **0.369**
- **mAP@0.5** from **0.610** to **0.644**
- **Precision** from **0.728** to **0.750**
- **Recall** from **0.524** to **0.550**

while achieving:

- **9.75M parameters**
- **20.5 GFLOPs**
- **4.6 ms/image** inference speed on **P1000 GPU**

These results show that the modified backbone provides a better accuracy–efficiency trade-off than the baseline YOLOv12s.

## Compared Models

The modified model was benchmarked against:

- YOLOv10s
- YOLOv11s
- Baseline YOLOv12s
- Attention-enhanced YOLOv12s variant

## Method

The backbone was modified by integrating lightweight attention mechanisms and optimized feature extraction components. Several configurations were tested to analyze their impact on:

- detection accuracy
- precision and recall
- parameter count
- FLOPs
- inference speed

The final selected configuration demonstrated the best overall improvement over the baseline.

## Experimental Results

| Model | Precision | Recall | mAP@0.5 | mAP@0.5:0.95 | Params | FLOPs | Speed |
|------|-----------|--------|---------|--------------|--------|-------|-------|
| YOLOv10s-100ep | 0.706 | 0.538 | 0.613 | 0.343 | 8.06M | 24.8G | 8.6 ms/img |
| YOLOv12s-100ep | 0.728 | 0.524 | 0.610 | 0.350 | 9.09M | 19.6G | 7.2 ms/img |
| YOLOv11s-100ep | 0.727 | 0.546 | 0.633 | 0.359 | 9.43M | 21.55G | 5.1 ms/img |
| Modified YOLOv12s | **0.750** | **0.550** | **0.644** | **0.369** | 9.75M | 20.5G | **4.6 ms/img** |

## Tech Stack

- Python
- PyTorch
- Ultralytics YOLO
- OpenCV
- NumPy
- Kaggle

## Repository Goals

- Modify YOLOv12 backbone for improved detection quality
- Evaluate lightweight attention modules in the backbone
- Compare accuracy and efficiency with baseline and other YOLO variants
- Analyze the trade-off between mAP improvement and computational cost

## Demo



## Future Work

- Explore additional lightweight attention modules
- Further reduce model complexity while preserving accuracy
- Test on more datasets and deployment environments
- Extend experiments to neck/head optimization

## Conclusion

This work shows that modifying the YOLOv12 backbone with lightweight attention mechanisms can improve object detection performance over the baseline model. The final variant achieved higher mAP, precision, recall, and faster inference speed, making it a strong candidate for efficient and accurate detection tasks.