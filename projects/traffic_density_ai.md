# Project STAR: Real-Time Computer Vision Adaptive Traffic Signal Control

### Context & Problem (Situation / Task)
* **Situation:** Urban traffic intersections suffer from static timer-based signal cycles, resulting in empty green lights while heavy traffic queues build on orthogonal lanes.
* **Challenge:** Deploying heavy deep-learning inference models to edge intersection controllers is cost-prohibitive, while cloud streaming introduces latency and connectivity risks.
* **Goal:** Build an adaptive, computer-vision-driven traffic control pipeline capable of real-time multi-lane vehicle density estimation and dynamic signal scheduling.

---

### Technical Solution & Architecture (Action)
* **Object Detection & Vehicle Tracking:** Trained and fine-tuned a YOLOv5 model optimized for multi-class vehicle detection (cars, buses, two-wheelers, trucks) across multiple video stream angles.
* **Density Computation Algorithm:** Developed a custom Python/OpenCV algorithmic pipeline to calculate lane vehicle volume, queue length, and waiting duration per junction quadrant.
* **Dynamic Green-Light Scheduler:** Replaced static timer loops with an adaptive scheduling algorithm that dynamically adjusts green-phase duration between 15s to 90s based on real-time density calculations.
* **Streaming Backend:** Integrated a Flask-based real-time telemetry server communicating with simulated signal controllers and live monitoring dashboards.

---

### Quantifiable Results & Impact (Result)
* **Detection Accuracy:** Achieved 94.2% mAP (mean Average Precision) across diverse weather and lighting conditions.
* **Congestion Reduction:** Simulated traffic flow tests showed a 28% reduction in intersection idle wait times and a 34% improvement in average vehicle throughput compared to fixed-time signals.

---

### ATS Resume Bullets (Ready to Paste)
* Developed an intelligent traffic signal optimization system utilizing YOLOv5 and OpenCV, achieving 94.2% mAP across multi-lane video streams.
* Designed an adaptive green-light scheduling algorithm in Python/Flask that reduced simulated intersection wait times by 28% compared to static timer cycles.
