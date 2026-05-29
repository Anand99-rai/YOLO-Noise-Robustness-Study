# Results and Analysis

## Overview

This research evaluates the robustness of modern YOLO object detection architectures under image degradation conditions. Models were tested using Gaussian Noise, Salt-and-Pepper Noise, and Poisson Noise applied at multiple intensity levels on a human-focused subset of the COCO dataset.

The following models were evaluated:

- YOLOv8n / YOLOv8s
- YOLOv9t / YOLOv9s
- YOLOv10n / YOLOv10s
- YOLO11n / YOLO11s
- YOLO26n / YOLO26s

Performance was measured using:

- Precision
- Recall
- mAP@50
- F1-Score
- Latency
- Robustness Retention Index (RRI)

---

# 1. Efficiency vs Robustness Trade-Off

<p align="center">
<img src="Results/Efficiency_vs_Robustness.png" width="900">
</p>

### Key Findings

- YOLOv9s achieved the highest robustness score under moderate noise.
- YOLOv10n provided strong robustness while maintaining very low inference latency.
- YOLOv9t achieved high accuracy but at the cost of increased latency.
- YOLOv10n offered the best overall trade-off between speed and robustness.

---

# 2. Latency Comparison

<p align="center">
<img src="Results/Latency.png" width="800">
</p>

### Observations

| Model | Approx. Latency |
|---------|---------|
| YOLOv10n | ~112 ms |
| YOLO11n | ~115 ms |
| YOLOv8n | ~119 ms |
| YOLO26n | ~233 ms |
| YOLOv10s | ~258 ms |
| YOLOv8s | ~270 ms |
| YOLOv9s | ~299 ms |
| YOLO26s | ~301 ms |
| YOLOv9t | ~353 ms |

**Fastest Model:** YOLOv10n

**Slowest Model:** YOLOv9t

---

# 3. Gaussian Noise Analysis

## mAP@50 Performance

<p align="center">
<img src="Results/mAP@50_Gaussian.png" width="900">
</p>

### Observations

- Gaussian noise caused the most severe degradation.
- Detection accuracy dropped rapidly beyond noise level 0.2.
- Most models completely failed at noise level 1.0.
- YOLOv9s retained the highest mAP under moderate Gaussian noise.

---

## F1 Score Performance

<p align="center">
<img src="Results/F1_Gaussian.png" width="900">
</p>

### Observations

- F1-score decreased sharply as Gaussian noise increased.
- YOLOv9s maintained the highest F1-score at moderate noise levels.
- Detection performance approached zero at extreme noise intensities.

---

# 4. Salt-and-Pepper Noise Analysis

## mAP@50 Performance

<p align="center">
<img src="Results/mAP@50_Salt_Pepper.png" width="900">
</p>

### Observations

- Salt-and-Pepper noise resulted in gradual performance degradation.
- Several models retained over 50% of their original mAP at moderate noise levels.
- YOLOv10n and YOLO11n demonstrated strong resilience.

---

## F1 Score Performance

<p align="center">
<img src="Results/F1_Salt_Pepper.png" width="900">
</p>

### Observations

- F1-score decreased steadily as noise density increased.
- YOLOv9s consistently maintained the strongest detection capability.
- YOLO26s showed the largest performance drop under severe noise.

---

## Recall Analysis

<p align="center">
<img src="Results/Recall_Salt_Pepper.png" width="900">
</p>

### Observations

- Recall decreased progressively with increasing corruption.
- YOLOv9s maintained the highest recall across most noise levels.
- All models eventually failed at extreme corruption levels.

---

## Robustness Retention Index (RRI)

<p align="center">
<img src="Results/RRI_Salt_Pepper.png" width="900">
</p>

### Formula

\[
RRI = \frac{mAP_{Noisy}}{mAP_{Clean}}
\]

### Observations

- YOLOv10n achieved the highest robustness retention.
- YOLO11n and YOLO26s also demonstrated strong resistance to Salt-and-Pepper noise.
- YOLOv8s exhibited the fastest decline in retained performance.

---

# 5. Poisson Noise Analysis

## mAP@50 Performance

<p align="center">
<img src="Results/mAP@50_Poisson.png" width="900">
</p>

### Observations

- Poisson noise had minimal impact on object detection.
- Most models maintained or slightly improved mAP values.
- Detection performance remained stable even at high noise levels.

---

## F1 Score Performance

<p align="center">
<img src="Results/F1_Poisson.png" width="900">
</p>

### Observations

- F1-scores remained consistently high.
- Several models showed slight improvements under Poisson noise.
- YOLO26s and YOLO11s achieved the highest F1 scores.

---

# Overall Findings

### Gaussian Noise

- Most destructive noise type.
- Significant degradation in mAP and F1-score.
- Models failed at high noise intensities.

### Salt-and-Pepper Noise

- Moderate degradation.
- Robustness varied significantly across architectures.
- YOLOv10n and YOLOv9s performed best.

### Poisson Noise

- Least harmful noise type.
- Detection performance remained stable.
- Some models benefited from slight contrast enhancement effects.

---

# Final Ranking

| Category | Best Model |
|-----------|-----------|
| Highest Robustness | YOLOv9s |
| Best Speed | YOLOv10n |
| Best Accuracy-Robustness Balance | YOLOv10n |
| Best Poisson Noise Performance | YOLO26s |
| Best Overall Deployment Choice | YOLOv10n |

---

# Conclusion

The study demonstrates that object detection robustness varies significantly across YOLO architectures when subjected to image degradation. Gaussian noise causes the greatest performance loss, while Poisson noise has minimal impact. Among all evaluated models, YOLOv9s achieved the highest robustness, whereas YOLOv10n provided the best balance of accuracy, robustness, and inference speed, making it the most suitable candidate for real-world deployment in autonomous systems, surveillance, robotics, and edge-AI applications.
