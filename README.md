# Post Process Pipeline (P3)

An astrophotrography image processing tool.

# Feature Targert

The following is a list of the target features for this project. If they're
crossed out, they exist in the project already.

1. Image Calibration
   - Dark Frame Subtraction: Removes sensor noise by subtracting dark frames
     (images taken with the same exposure but with the lens cap on).
   - Flat Field Correction: Corrects for vignetting and dust by using flat
     frames (images of a uniformly lit source).
   - Bias Frame Subtraction: Removes readout noise from the sensor using bias
     frames (images taken with the shortest possible exposure).
2. Alignment and Registration
   - Star Alignment: Accurately align all images based on star positions to
     compensate for slight misalignment between frames.
   - Subpixel Accuracy: Ensures that even small misalignments are corrected to
     maximize the sharpness of the final stacked image.
   - Multiple Transformation Models: Support different transformations like
     translation, rotation, scaling, and possibly distortion correction for lens
     effects.
3. Image Stacking
   - Median/Average Stacking: Combine multiple frames to reduce noise and
     improve signal.
   - Sigma Clipping: Reject outlier pixels that may be caused by cosmic rays,
     satellites, or other artifacts.
   - Weighted Stacking: Give better-quality frames more weight in the final
     stack to improve overall image quality.
4. Noise Reduction
   - Multi-scale Noise Reduction: Implement noise reduction techniques that act
     on different spatial scales, preserving fine details while reducing noise.
   - Adaptive Filtering: Allow fine-tuning of noise reduction based on local
     image content (like smoothing areas with little detail and preserving edges).
5. Dynamic Range Compression
   - Histogram Stretching: Adjust the image's dynamic range to make faint
     details more visible.
   - Local Contrast Enhancement: Enhance the contrast in specific regions to
     bring out faint structures.
6. Color Calibration
   - White Balance: Correct the color balance in images, especially for RGB
     data.
   - Background Neutralization: Automatically adjust the background color to be
     neutral (important in astrophotography where light pollution can skew colors).
7. Star Masking
   - Automatic Star Detection: Detect stars and separate them from the
     background, so you can treat stars and the background separately in
     processing.
   - Star Reduction: Reduce the prominence of stars to bring out faint nebulae
     or other objects.
8. Stretching and Tonemapping
   - Asinh Stretching: Non-linear stretching that helps preserve star colors
     while bringing out faint details.
   - HDR Composition: Stack images taken with different exposures to retain
     detail in both bright stars and faint objects.
9. Automation and Scripting
   - Batch Processing: Allow for the processing of multiple images
     automatically using scripts.
   - Custom Pipelines: Enable users to build custom processing pipelines to suit
     their needs.
10. Output Support
    - Fits Support: Ensure compatibility with FITS files, which are commonly
      used in astrophotography.
    - Export Formats: Allow export to common image formats (TIFF, PNG, JPEG)
      for further processing or sharing.
11. GUI
    - Node Editor: Ability to build pipelines, save them, load them from a
      node/graph editor.
    - Image Preview: Add image preview and ability to pause at any portion of
      the pipeline to inspect the work.
