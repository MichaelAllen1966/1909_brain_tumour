# 2002_brain_tumour
> Kaggle brain tumour scan

A short introduction to image processing using Neural Nets to detect tumours in brain scans. This uses a Kaggle image data set.

## Quick Start
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/MichaelAllen1966/2009_brain_tumour/master)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MichaelAllen1966/2009_brain_tumour)

### Colab
1. When running in Colab, before running the code, select `Runtime, Change runtime type` and select `GPU`
2. As Google doesn't persist data, set the `Download Data` parameter to `True` to download the data to the Google Cloud storage temporarily

## Code Outline
To speed things up the images are converted to greyscale using the `cv2.imread()` function. Images are cropped to the limit of the brain scan using simple light and dark analysis. Keras manages image rotation and reflection so that doesn't need to be managed in the code.
