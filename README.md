# Image_Segmentation_Unet_ViT

![image](https://github.com/user-attachments/assets/c22c09d8-c228-4326-aeb4-a15a55c92ad4)

Satellite Image Multiclass Segmentation using U-net and ViT Deep Learning Models.

**Dataset Link** : https://humansintheloop.org/resources/datasets/semantic-segmentation-dataset-2/

**Dataset Description**: This open-access dataset contains aerial footage acquired over Dubai by MBRSC satellites and 
rigorously annotated with pixel-level semantic segmentation across six unique 
classifications. The dataset contains 72 photos, which are organised into six larger tiles for easy management and analysis. 
The annotated classifications are Building, Land (unpaved area), Road, Vegetation, Water, and Unlabeled, with each represented by a distinct hexadecimal colour code for pixel identification.
This dataset serves as a valuable resource for advancing research in remote sensing and deep learning applications, particularly in the domain of land cover mapping and urban area analysis. 

**Models Used **

**U-Net**: 

 **Architecture**: encoder/decoder with skip connections. 
 **Purpose**: Semantic segmentation, particularly in medical imaging. 
 **Layers included**: DoubleConv, Down, Up, and OutConv. 
 **Training**: Use the Focal Loss feature to address class imbalance.
 
 The U-Net model is a convolutional neural network (CNN) architecture intended for 
semantic segmentation tasks, specifically medical image segmentation. It is composed 
of an encoder-decoder structure with skip links between the encoder and decoder layers. 
This design facilitates the effective capture of both local and global context information. 
The input image is downsampled by the encoder using a succession of convolutional 
and pooling layers, and the feature maps are upsampled by the decoder to create the 
segmentation mask. In this version, the U-Net architecture consists of convolutional 
layers (DoubleConv), downsampling layers (Down), upsampling layers (Up), and a 
final convolutional layer for output. The U-Net model is trained with a Focal Loss 
function, which is a type of cross-entropy loss meant to overcome class imbalance in 
segmentation tasks.

 **Vision Transformer (ViT)**: 
 
  **Architecture**: Transformer-based for image processing 
  **Purpose**: Originally designed for picture classification, but now adapted for 
               segmentation. 
  **Components**: Self-attention layers, FeedForward layers, Transformer blocks. 
  **Training**: Focal Loss function for addressing class imbalance.
  
The Vision Transformer (ViT) model is a novel method to image processing, originally 
designed for picture classification and then repurposed for semantic segmentation. ViT 
takes a unique approach, expressing images as sequences of patches that are 
subsequently processed by transformer-based encoder layers. This architectural 
paradigm shift allows ViT to successfully capture global dependencies and spatial 
interactions inside an image, which is critical for correct semantic segmentation. Self
attention mechanisms, multi-layer perceptron (MLP) blocks, and transformer modules 
are all essential components of the ViT implementation. Depending on the setup, the 
model's output is pooled by computing the sequence's mean or using a class token (CLS 
token). Similar to U-Net, ViT uses the Focal Loss function during training to solve class 
imbalance and optimize segmentation performance.

Result:
[Epoch 4/5] [Batch 16/17] [Loss: 1.140521 (0.713330)] epoch 4 - loss : 0.71333 - acc : 0.70 - val loss : 0.69283 - val acc : 0.72
![image](https://github.com/user-attachments/assets/2892af6c-d020-43e2-b232-0e506be54d74)
![image](https://github.com/user-attachments/assets/b0cc9894-8f1d-4375-891d-b61bd6441a35)


**NOTEBOOK LINK** : https://shorturl.at/sE0TP



  

  
