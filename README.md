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

Use SciKitLearn to split into Training and Test data; this should really be done with k-fold validation. The `reshape()` puts it into an array form acceptable to Tensorflow; image files typically have 3 arrays of colours so 3 channels (RGB) which is represented as 3 arrays (each channel is read left-right, top-bottom), these are all wrapped in an array, ie. for a 4 pixel image: `[[r0, r1, r2, r3], [g0, g1, g2, g3], [b0, b1, b2, b3]]`. A grey-scaled array which has but one channel has `[[grey0, grey1, grey2, grey3]]` since Tensorflow expects the same array structure.
