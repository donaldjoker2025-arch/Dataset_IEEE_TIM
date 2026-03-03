# Dataset_IEEE_TIM

## Indoor Geomagnetic Positioning Dataset
> Associated with the paper submitted to **IEEE Transactions on Instrumentation and Measurement**:  
> *"A Quality-Driven Geomagnetic Measurement Framework for Indoor Positioning: Fingerprint Distinguishability Analysis and Robust Trajectory Matching"*

---

## 📂 Released Datasets

The following datasets have been made publicly available:

| Scenario | Training Set | Test Set |
|----------|-------------|----------|
| **Corner** | ✅ | ✅ |
| **Corridor** | ✅ | ✅ |

---

## 📋 Data Format

Each dataset is provided as a preprocessed CSV file containing the following fields:

### Input Features

| Field | Description |
|-------|-------------|
| `group` | Trajectory group index |
| `time` | Timestamp |
| `yaw` | Yaw angle (deg) |
| `pitch` | Pitch angle (deg) |
| `roll` | Roll angle (deg) |
| `qx`, `qy`, `qz`, `qw` | Quaternion components |
| `mag_x_n`, `mag_y_n`, `mag_z_n` | Calibrated geomagnetic field (ENU frame, μT) |

### Output Labels

| Field | Description |
|-------|-------------|
| `x` | Relative X coordinate (m) |
| `y` | Relative Y coordinate (m) |

---

## 🚀 Quick Start

```python
import pandas as pd

train_df = pd.read_csv('corner_train.csv')
test_df  = pd.read_csv('corner_test.csv')

mag_cols = ['mag_x_n', 'mag_y_n', 'mag_z_n']
label_cols = ['x', 'y']
```

---

## 📄 Citation

If you use this dataset in your research, please cite:

```
@article{wang2025geomagnetic,
  title   = {A Quality-Driven Geomagnetic Measurement Framework for Indoor Positioning},
  author  = {Wang, Jiale and Ren, Zhanyan and Zhang, Zhanpeng and Xia, Ming and Shi, Chuang},
  journal = {IEEE Transactions on Instrumentation and Measurement},
  year    = {2025}
}
```

---

## 🤝 Contact & Collaboration

We warmly welcome further research, discussions, and collaborations using these datasets.  
Feel free to open an **Issue** or reach out via email.

---

<p align="center">
  <img src="https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg" alt="License"/>
  <img src="https://img.shields.io/badge/Platform-IEEE%20TIM-blue.svg" alt="IEEE TIM"/>
  <img src="https://img.shields.io/badge/Status-Active-brightgreen.svg" alt="Status"/>
</p>
