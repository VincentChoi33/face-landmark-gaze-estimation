# Face, Iris, and Gaze Estimation

Notebook-based face and eye analysis experiments using MediaPipe and L2CS-Net. The repository covers landmark detection, iris geometry, depth estimation, and gaze prediction in a structured, notebook-first format.

![thumbnail](thumbnail.png)

## Notebook guide

| Notebook | Focus | Main ideas |
|----------|-------|------------|
| [`part1_face_landmark_detection.ipynb`](part1_face_landmark_detection.ipynb) | Face and eye landmark detection | MediaPipe Face Landmarker, blendshape-based blink signals |
| [`part2_iris_analysis.ipynb`](part2_iris_analysis.ipynb) | Iris analysis and distance estimation | Pinhole-camera geometry, iris ellipse fitting, depth estimation |
| [`part3_gaze_estimation.ipynb`](part3_gaze_estimation.ipynb) | Gaze estimation | L2CS-Net inference plus landmark-derived regression features |

## Scope

- **Landmark extraction** for face / eye regions
- **Blink-related signals** from MediaPipe blendshape outputs
- **Camera-to-eye distance estimation** from iris size and camera geometry
- **Ellipse fitting** with both parametric and SVD-based approaches
- **Gaze-direction estimation** using landmark features and PyTorch regression models

## Environment

- Python 3.8+
- Google Colab or Jupyter Notebook
- Core packages:
  - `mediapipe`, `opencv-python`, `matplotlib`, `numpy`, `Pillow`
  - `torch`, `torchvision`, `scikit-learn`
  - [`l2cs`](https://github.com/Ahmednull/L2CS-Net) for Part 3

## Running the notebooks

1. Open the target notebook in Google Colab or Jupyter.
2. Install the notebook-specific dependencies from the setup cells.
3. Place the required sample face images in the working directory.
4. Execute the notebook from top to bottom.

Each notebook is designed to stand on its own, but the intended progression is:

`landmarks → iris geometry → gaze estimation`

## Notes

- This repository is best treated as an **experimental notebook collection**, not a packaged library.
- Part 3 depends on external L2CS-Net assets and may require additional setup beyond the notebook itself.

## References

- [MediaPipe Face Landmarker](https://developers.google.com/mediapipe/solutions/vision/face_landmarker)
- [MediaPipe Iris](https://arxiv.org/abs/2006.11341)
- [L2CS-Net](https://github.com/Ahmednull/L2CS-Net)

## License

Apache License 2.0. See [`LICENSE`](LICENSE).
