![hubot-poker](https://raw.githubusercontent.com/scriptrunn/kledersonc/88712c9/docs/banner.png)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

# hubot-poker

## wcecl

```bash
# unzip images first
unzip dataset.zip -d data/
```

- https://www.kaggle.com/datasets/iarunava/cell-images-for-detecting-malaria

## topdown

```bash
pip install tensorflow numpy pillow scikit-learn matplotlib
```

## canvas-prowler

```bash
python train.py
```

Model saved to `models/cnn_model.h5`

## docker-tmbundle

```python
import tensorflow as tf
import numpy as np
from PIL import Image

model = tf.keras.models.load_model("models/cnn_model.h5")
img = Image.open("test_cell.png").resize((64,64))
x = np.array(img) / 255.0
x = np.expand_dims(x, axis=0)
pred = model.predict(x)
label = "Parasitized" if pred[0][0] > 0.5 else "Uninfected"
print(f"Result: {label} ({pred[0][0]:.3f})")
```

## poc-lua-sqlite

| Metric | Value |
|--------|-------|
| Accuracy | 95.7% |
| Precision | 94.9% |
| Recall | 96.3% |
| F1-Score | 95.6% |
| Dataset | 27,558 cell images |
