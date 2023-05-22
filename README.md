# Spectral Angle Technique to perform image classification


Spectral Angle Classification is a technique used for image classification in remote sensing. It measures the spectral similarity between pixels in an image by computing the angle between their spectral vectors in a high-dimensional feature space. The underlying principle is that pixels belonging to the same class exhibit similar spectral signatures.

Here's a detailed explanation of how Spectral Angle Classification works:

1. **Spectral Signatures**: Each pixel in a hyperspectral image is represented by a spectral signature, which is a vector of spectral reflectance or radiance values across different bands of the electromagnetic spectrum. These bands can range from visible to near-infrared and beyond.

2. **Reference Spectra**: In order to classify pixels, we need reference spectra that represent the spectral signatures of known classes. These reference spectra are typically obtained by selecting representative pixels from ground truth data or expert knowledge.

3. **Normalization**: Before computing the spectral angle, it is important to normalize the spectral signatures. Normalization ensures that differences in illumination, atmospheric conditions, and sensor response are accounted for. Common normalization methods include scaling the spectral vectors to unit length or subtracting the mean and dividing by the standard deviation.

4. **Spectral Angle Calculation**: The spectral angle between a pixel's spectral signature and a reference spectrum is calculated using a geometric interpretation. It is determined by the angle between the two vectors in the feature space. The smaller the angle, the more similar the spectra and the higher the likelihood of the pixel belonging to the corresponding class.

5. **Classification Decision**: Once the spectral angle is computed, a classification decision is made based on a predefined threshold. If the angle is below the threshold, the pixel is classified as belonging to the corresponding class; otherwise, it is classified as a different class or labeled as unclassified.

6. **Threshold Determination**: Setting an appropriate threshold is crucial for accurate classification. The threshold can be determined empirically based on the specific dataset and application requirements. It should balance between classifying pixels correctly while avoiding false positives or false negatives.

7. **Iterative Classification**: In some cases, the classification process may involve multiple iterations. Initially, all pixels are unclassified, and as the classification proceeds, the labels of already classified pixels are used to refine the classification of neighboring or similar pixels. This iterative approach can improve the overall accuracy of the classification.

Spectral Angle Classification offers several advantages, including its ability to handle mixed pixels, sensitivity to spectral variations, and robustness to noise. However, it assumes that the spectral differences between classes are primarily due to differences in composition and not due to other factors such as illumination or view angle.

With the following repository I have provided the following jupyter notebook where a classification task with spectral angle is performed.
