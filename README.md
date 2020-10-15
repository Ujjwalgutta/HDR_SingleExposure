# Deep HDR Video Reconstruction Using Single Exposure

## Motivation
- Reconstruction of saturated image regions to recover lost information.
- HDR displays which are widely used everyday in the world use this technology.

## Data Augmentation
Realistic Camera Curve using sigmoid function.
![Alt Text](Images/DataAug.PNG)


## AutoEncoder Model Architecture
The model is a Convolutional Neural Network in form of a Hybrid Dynamic Range Encoder. VGG-16 architecture without any fully connected layers is used. Skip-Connection layers from encoder to decoder at each level of resolution. 
![Alt Text](Images/AutoEncoder.PNG)

## Alpha-Blending
Prevents banding artifacts between predicted highlights and their surroundings. Keeps the input image unmodified in the non-saturated regions.
![Alt Text](Images/AlphaBlending.PNG)

## Results
### Video

Input LDR Video          |        Reconstructed HDR Video
:-------------------------:|:-------------------------:
![Alt Text](Videos/input_video.gif) | ![Alt Text](Videos/output_video.gif)

### Images

Input LDR Image          |        Reconstructed HDR Image
:-------------------------:|:-------------------------:
<img src="Images/LDR_img.PNG" width="400" height="400">   |   <img src="Images/HDR_img.PNG" width="400" height="400">

## References
[1] 
 
