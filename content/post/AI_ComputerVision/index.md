---
title: "Bee Detection and Tracking at Hive Entrance using YOLO11 and ByteTrack"
description: 
date: 2026-08-29T05:31:28Z
image: coverAI.png
math: 
license: 
comments: true
draft: false
build:
    list: always    # Change to "never" to hide the page from the list
---
## 🐝 Bee Tracking and Counting with YOLOv11 + ByteTrack 

> 📄 **[Read the Research Paper on arXiv →](https://arxiv.org/abs/2608.23213v1)**

{{< youtube kIclX8NpDqc >}}


Developed an automated bee monitoring system using **YOLO11 + ByteTrack** to detect, track, and count bees entering and leaving a hive.

* **Data augmentation:** Compared light vs. heavy augmentation and found that **moderate augmentation** performed better for small bee objects. Heavy techniques such as RandAugment and random erasing degraded localization and recall.
* **Backbone training:** Evaluated full fine-tuning, full backbone freezing, and **progressive backbone unfreezing**. Freezing the backbone during the first 30 epochs before fine-tuning achieved the best balance of stability and localization, reaching **~98.7% mAP50** and **~0.78 mAP50-95**.
* **ByteTrack optimization:** Tuned detection thresholds and tracking parameters to handle **low-confidence detections, occlusion, and fast bee movement**. Lower confidence thresholds and a longer track buffer improved trajectory continuity, while a higher matching threshold helped reduce ID switches.
* **Results:** Correctly counted **43/47 incoming bees (91.5%)** on an independent 25 FPS video.

**Tech:** Python · YOLO11 · ByteTrack · Computer Vision · Object Detection · Multi-Object Tracking