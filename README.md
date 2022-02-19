# PDAC_Prediction

## A Novel Multiresolution-Statistical Texture Analysis Architecture: Radiomics-Aided Diagnosis of PDAC Based on Plain CT Images

Step-by-Step

1. The number of pixels in these ROIs may be different. We normalized the texture features of an ROI based on the number of pixels in this ROI.
2. Multiresolution analysis decomposes an ROI into multiple low-/high-frequency sub-band components. A component is expressed by a coefficient matrix. A coefficient can represent a grayscale change in a local range.
3. We randomly divided the dataset (i.e., the ROIs) into a training set and a test at a ratio of 7:3.
4. Wavelet2D - 2 level (8 components)
    1. Group by component number
    2. Group by Label
    3. Find AVM
    4. Find Appropriate intervals
5. Discretize ROIs
6. Statistical Analysis and feature extraction
    1. Histogram
    2. Co-efficient statistics
    3. Co-occurrence matrix
    4. Run-length matrix
7. Feature selection (training dataset)
    1. ILFS - infinite latent feature selection algorithm :  rank the features based on the training set and selected the first k features. (k<20)
8. Classification
    1. SVM
9. Significance Testing
    1. Mann-Whitney U test