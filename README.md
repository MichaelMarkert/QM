## What does the imageQM Tool do?

imageQM (https://michaelmarkert.github.io/QM/imageQM) is a web-based tool that provides basic feedback on formal image quality, with a focus on object photography in GLAM institutions (Galleries, Libraries, Archives, and Museums). 

**Privacy first:** All image evaluation happens locally in your browser—your pictures never leave your computer and no server copies are generated.

The tool can also run completely offline. Simply download all files from the repository (.html + .js) to the same folder and open the HTML file in your browser.

## How to use it

1. **Load an image:** Click the `Evaluate image (no upload)` button and select your image file (.jpeg, .png, or .tiff)
2. **Check composition margins:** Click `Toggle margins` to display areas (typically 5% on three sides, 10% on the bottom) that should remain free of object elements for optimal aesthetics
3. **View composition guides:** Click `Toggle grid overlay` to display:
   - Rule of thirds lines for balanced composition
   - 45° diagonal lines to assist with proper object rotation on your photography table

## Understanding the evaluation results

### EXIF Data
The tool displays available metadata from your image file, including camera settings and capture information.

**Red values indicate potential sharpness issues.** When ISO, aperture, or shutter speed values appear in red (exceeding recommended thresholds), your image may be blurry or the object may not be as sharp as possible. Carefully review the image at 100% zoom to verify sharpness.

## Edge Distribution Analysis

This metric analyzes the average RGB values of 10 random pixels along each of the four edges (top, bottom, left, right) and serves two important purposes:

**a) Lighting evenness**  
Edge distribution shows whether light is evenly distributed across the image. If values along one or two edges are significantly higher or lower than others, you may need to adjust the intensity, angle, or position of your lights.

**b) White balance accuracy**  
Each edge displays RGB values. If the red, green, and blue values differ by more than 3 points (e.g., R:235, G:248, B:245), your white balance is off and needs correction.

### Extreme Pixel Values

The tool counts pixels with extreme values:
- **Pure black (0,0,0)** 
- **Pure white (255,255,255)**

**Acceptable threshold:** These values should each be near 0% of total pixels. Higher percentages indicate:
- Too many pure white pixels → image is overexposed
- Too many pure black pixels → image is underexposed
