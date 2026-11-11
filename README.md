# DH307 — Oral Lesion Segmentation Experiments

Course project exploring segmentation of oral potentially malignant disorder (OPMD) images:
image enhancement, U-Net variants, attention gates, and modern detection/segmentation models.

## Contents

| Area | Files |
| --- | --- |
| Preprocessing / enhancement | `image_enhancement.ipynb`, `augmentated.ipynb` |
| U-Net | `unet.ipynb`, `vanilla_unet.ipynb`, `unet_image_enhanced.ipynb`, `simple_multi_unet_model.py` |
| Attention U-Net | `AttentionUnet/*.ipynb` |
| Instance / panoptic segmentation | `maskrcnn.ipynb`, `sam2.ipynb` |
| YOLO | `yolov5.ipynb`, `yolov5/` (upstream, not bundled) |
| Feature analysis | `FeatureVisualization.ipynb` |
| Notes / reports | `DOCUMENTATION.docx`, `*.pdf` |

Trained weights under GitHub's 100 MB file limit are included:
`unet_model.pth`, `yolov5s.pt`, `yolov8n.pt`, `yolov8s-seg.pt`.

## Not included

To keep the repository small and avoid publishing clinical images, the following are
ignored by `.gitignore`:

- `OPMD_new-*.zip` (dataset archive) and the `test_practice/` images
- image folders: `enhanced_images/`, `labelled_images/`, `augmented_images/`, `augmented_masks/`
- backbone weights: `res34_backbone_50epochs*.hdf5`
- training runs (`runs/`), `logs/`, Jupyter checkpoints
- third-party clones: `yolov5/`, `AttentionUnet/Attention-Gated-Networks/`

## Running

`data.yaml` currently contains absolute local paths; update `train`, `val`, and `masks`
to point at your own dataset before training.
