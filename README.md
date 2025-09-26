# Sat-Images-Water-Segmentation-Pretrained-Model-with-deployment

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)


### Notebook Highlights

* Matched the correct masks to images, since there are more masks than images in the dataset folder.

* I applied Min Max Scaler for Normalization instead of dividing by 255 because for some bands, the pixel intensity is above 255.

* * Visualized each band of the images

* Computed water indices to add more band that will be more beneficial for the model to understand the water bodies like:
*  * **NDWI – Normalized Difference Water Index**
   * **MNDWI - Modified NDWI**
   * **AWEI_SH - Automated Water Extraction Index (Shadow version)]**
  
Then added these water indices as extra channels to the 12 existing channels of the SAT images. 

* Applied different Augmentation using `albumentations` and applied the same augmentations for both the images and the corresponding masks.

* **Fine-Tuned a pretrained model** `res-net 34` and loaded ImageNet weights for 3 channels out of the 15 (12+3) using `PyTorch`.

* Visualized the Model's **losses** and **IOU** curves.

* Evaluated the model by **IOU**, **rcall**, **precision**, **f1 score** metrics

* Visualized the `Satellite Image`, `Ground Truth Mask` and the `Predicted Mask`.

* Deployed the model by using `streamlit` and `Ngrok`.

### Sample pics

<img width="1366" height="686" alt="Screenshot (1629)" src="https://github.com/user-attachments/assets/ac05f48d-bb97-446a-880b-2edc2c63e8fb" />

<img width="1366" height="683" alt="Screenshot (1630)" src="https://github.com/user-attachments/assets/99e6e482-a5e1-4cf8-99d9-a7b39772ec36" />

<img width="1366" height="688" alt="Screenshot (1631)" src="https://github.com/user-attachments/assets/4c34110a-645a-4e1f-8fbf-31a6c24d28ec" />

<img width="1366" height="680" alt="Screenshot (1632)" src="https://github.com/user-attachments/assets/c56adc40-b265-4219-991b-64445870c3ee" />

<img width="1366" height="613" alt="Screenshot (1633)" src="https://github.com/user-attachments/assets/9b8657da-6317-49f2-b30d-7ae3d36f2e8b" />

