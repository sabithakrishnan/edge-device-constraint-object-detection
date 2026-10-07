# Edge AI Stream Simulation: OpenVINO & Frame Skipping

A Python-based simulation demonstrating how to deploy real-time object detection models on resource-constrained devices, such as a Raspberry Pi or low-power edge gateways. 


---

## 🚀 Key Features & Edge AI Concepts

* **Hardware Optimization (OpenVINO FP16):** Compresses standard model weights to half-precision (FP16), lowering memory overhead and maximizing inference throughput on edge CPUs.
* **Intelligent Frame Skipping:** Processes every N-th frame (e.g., every 3rd frame) to drop CPU load by up to 66% while persisting bounding boxes to prevent visual flickering.
* **Targeted Inference Class Filters:** Restricts detection pipelines specifically to vehicle categories (cars/trucks), eliminating downstream post-processing bottlenecks.
* **Headless Display Emulation:** Simulates real-time edge processing constraints alongside a live rendering preview window directly in a browser notebook environment.

---

## 📦 Prerequisites

Ensure you have the following packages installed before running the simulation. If you are executing this inside Google Colab, you can install the core requirements via pip:

```bash
pip install ultralytics openvino opencv-python numpy
```

---

## 🖥️ Getting Started
   * **1-video Stream:** Generates a synthetic `.mp4` video file if a live local camera capture source or sample file isn't present.
   * **2-Model Compilation:** Automatically downloads standard weights (`yolov8n.pt`) and exports them into optimized static OpenVINO structures (`yolov8n_openvino_model/`).
   * **3-Streaming Inference Loop:** Launches the frame-skipping pipeline with a persistent real-time FPS performance benchmark counter printed onto the frames.

---



