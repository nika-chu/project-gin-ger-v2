# Dependencies

Training runs on **Kaggle GPU** (T4). Jetson uses exported ONNX/TensorRT only.

4-split Kaggle notebooks

## data\_preparation

| Package | Purpose |
| :---- | :---- |
| torch 2.5.1 \+ cu124 | GPU (installed in notebook if image PyTorch broken) |
| torchvision 0.20.1 | Bundled with torch |
| roboflow | Download COCO dataset |
| scikit-learn | Stratified train/valid/test split |

## DeiT Training

| Package | Purpose |
| :---- | :---- |
| transformers | DeiT-Small-Distilled, Trainer |
| datasets | HuggingFace dataset pipeline |
| accelerate | Trainer backend |
| matplotlib | Confusion matrix, loss plots |
| scikit-learn | Metrics, 5-fold CV |
| torch, torchvision | Already in data\_preparation |

## Faster R-CNN

| Package | Purpose |
| :---- | :---- |
| torch, torchvision | Faster R-CNN ResNet50-FPN V2 |
| pycocotools | COCO bbox format |
| matplotlib | Loss plots |

## Export/Integration

| Package | Purpose |
| :---- | :---- |
| torch, torchvision | ONNX export |
| transformers | Load saved DeiT weights |
| matplotlib | For demo  |

## Jetson Nano (inference only)

| Component | Version |
| :---- | :---- |
| JetPack | 4.6 |
| CUDA | 10.2 |
| TensorRT |  |
| ONNX files |  |

Do not install full HuggingFace stack on Jetson. 
