# Inpainting_GIT_Images
This repository contains notebooks that follow the procedure of inpainting on medical images. The dataset used is KVASIR from Kaggle and a UNET architecture has been used for training a segmentation model. 

For inpainting, stable-diffusion inpainting model from runway-ml has been used. 
https://huggingface.co/runwayml/stable-diffusion-inpainting

To access the pretrained UNET model you can click on the following link.
https://drive.google.com/drive/folders/1d206ZpTpq_6pV2geQvJPoXFCaVQ5lIoe

## How to Make It Work
1. First you need to open the SegmentationUnetModel notebook and train a segmentation model on the Kvasir Dataset.
2. With the model trained you can then give example images and create masks of the polyps and tumors in the images.
3. When you have the masks you can then save them and the original images.
4. Open the InpaintingMedicalImaging notebook and then inpaint the images.
5. There are a few examples added in the repository that have been used in the Inpainting notebook.

### Restrictions
The model hallucinates a bit so you have to play around with the prompt, the number of inference steps and the guidance scale to get the optimal results.
In case the polyp/tumor is too big, the model will find it difficult to completely inpaint and hallucinate to create random shapes in the images 
