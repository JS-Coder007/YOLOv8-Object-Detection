# DESCRIPTION:
|![YOLOv8 Object Detection Example](https://raw.githubusercontent.com/JS-Coder007/YOLOv8-Object-Detection/refs/heads/main/doc/img/detected_objects.jpg)
  *Original image source: [Flickr - Nicole Lee](https://www.flickr.com/photos/nicolelee/19041780)*

  # ⚠️ Important Note

  * Input images are resized directly to fit the model’s expected input dimensions.
  * Padding is **not** applied, which may reduce accuracy if your images have a different aspect ratio than the model’s input size.
  * To maintain performance, try to use input sizes that closely match the aspect ratio of your images.

---

# 📦 Requirements

* Refer to the `requirements.txt` file for dependencies.
* If you're using a **NVIDIA GPU**, install `onnxruntime-gpu`.
  Otherwise, install the standard `onnxruntime`.

---

# 🛠️ Installation

```bash
git clone https://github.com/ibaiGorordo/ONNX-YOLOv8-Object-Detection.git
cd ONNX-YOLOv8-Object-Detection
pip install -r requirements.txt
```

### ONNX Runtime Setup

* For systems with **NVIDIA GPU**:

  ```bash
  pip install onnxruntime-gpu
  ```
* For CPU-only systems:

  ```bash
  pip install onnxruntime
  ```

---

# 🔄 Convert YOLOv8 to ONNX

Use the Google Colab notebook to export the model:
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1-yZg6hFg27uCPSycRCRtyezHhq_VAHxQ?usp=sharing)

Alternatively, convert using Python with Ultralytics:

```python
from ultralytics import YOLO

model = YOLO("yolov8m.pt")
model.export(format="onnx", imgsz=[480, 640])
```

---

> 💡 The original YOLOv8 models were converted to ONNX and other formats by [PINTO0309](https://github.com/PINTO0309).
> You can download them from his [model zoo repository](https://github.com/PINTO0309/PINTO_model_zoo/tree/main/345_YOLOv8).
> Either run the `download_single_batch.sh` script or manually download and place the ONNX files (e.g., `yolov8m_480x640.onnx`) into the `models` directory.
> Make sure to update your script with the correct filename if needed.

---

# 📁 Original YOLOv8 Repository

* Source: [ultralytics/ultralytics](https://github.com/ultralytics/ultralytics)
* License: [GPL-3.0 License](https://github.com/ultralytics/ultralytics/blob/main/LICENSE)

---

# 🚀 Example Usage

### 🔹 Image Inference

```bash
python image_object_detection.py
```

### 🔹 Webcam Inference

```bash
python webcam_object_detection.py
```

---

# 🔗 References

* [Ultralytics YOLOv8](https://github.com/ultralytics/ultralytics)
* [PINTO0309 Model Zoo](https://github.com/PINTO0309/PINTO_model_zoo)
* [Model Conversion Tools (OpenVINO → TensorFlow)](https://github.com/PINTO0309/openvino2tensorflow)

---
