# Cell_morphology_stats
A python script to measure cell morphology features using phase contrast images.
## Aim of the tool 
The aim of this Python workflow is to quantify and compare key morphological features—specifically Length (Major Axis), Area, and Circularity—of cells captured via phase contrast microscopy. This can be used to detect and measure phenotypic changes between experimental groups (e.g., control vs. treatment).
## How to use
1. Use image editing software to simply adjust the brightness, contrast and sharpness of the original phase contrast photo (e.g. example_data/testwt.jpg) to black and white images (e.g. example_data/testwt2.jpg).
2. Install required python modules
```
pip install cv2
pip install numpy
pip install pandas
pip install matplotlib
```
3. Run the jupyter notebook("Phase_contrast_photo_morphology.ipynb")
Set configurations: use the adjusted image (e.g. example_data/testwt2.jpg) as input, and adjust the MIN_SIZE_THRESHOLD based on the final contors overlay results in the output (green lines dipicts cell outlines).
4. Results description
1) Cell area: the count of all pixels enclosed by the green line (unit, pixels^2);
2) Circularity: A ratio derived from the perimeter (length of the green line) and the enclosed area (4 * np.pi * area / (perimeter * perimeter). 
3) Length: the longest distance between two points on the green outline (major axis of the fitted ellipse; unit: pixels). 
