# Stable-Diffusion-Textual-Inversion-Image-Generation-Model-Using-Fast-Diffusion
This project contains the custom model created using the DreamBooth Model and Lora for textual inversion based on a custom training dataset. This model was created using fast stable diffusion version 1.5. This model uses textual inversion to generate new images based on text injections. The model is trained on 15 512 x 512 jpg images with 1100 U-Net training steps. Model was trained on Google Virtual Machines through the Colab jupyter environment.
<br/><br/>Example Image:<br/>
![00000-3673782264](https://user-images.githubusercontent.com/127776575/229376096-2b8eb215-4887-4154-b750-562312358c41.png)

This repository contains the Stable Diffusion Textual Inversion Image Generation Model, an AI model that applies textual inversion for generating images. Based on the Fast Diffusion approach, this model was built using DreamBooth Model and Lora on a custom training dataset.

The core principle of the model is to generate new images based on text injections, utilizing a Stable Diffusion algorithm. The model was trained on 15 512 x 512 jpg images with 1100 U-Net training steps on Google Virtual Machines via the Colab Jupyter environment.

# Getting Started
First, clone this repository:

bash
Copy code
```
git clone https://github.com/username/Stable-Diffusion-Textual-Inversion-Image-Generation-Model-Using-Fast-Diffusion.git
```

You will need Python 3.6+ and the packages mentioned in requirements.txt. Install these packages using pip:

bash
Copy code

```
pip install -r requirements.txt
```

# Model Architecture
This model is constructed on a Stable Diffusion framework, where the textual inversion approach generates images based on the text inputs. The model utilizes a U-Net for training and Lora for textual inversion. The process follows the principle of Diffusion Models where the final image is seen as a result of applying a series of transformations (diffusion steps) on a noise vector. The idea is to teach the model to reverse this process.

# Technical Details
The Stable Diffusion Model we use here is v1.5. We used U-Net for training with 1100 training steps. The input data consists of 15 512x512 jpg images. We utilized Lora for textual inversion.

The model architecture consists of three main components:

A U-Net which takes in the image and maps it to a latent space representation.
A diffusion model which adds noise to the latent space representation to create new images.
A textual encoder which maps the text inputs to a latent space.
The model is trained using a mixed precision training method for efficiency. The training involves applying the textual inversion on the images in the dataset, where the model learns to generate images from text inputs.

# How to Use
Before proceeding with model training, you need to prepare your dataset. The model requires a dataset of 15 512 x 512 jpg images. Make sure to provide the correct path of the dataset.

For training, follow these steps:

1. Load the dataset
2. Define your model parameters
3. Train the model using the pre-defined U-Net architecture
4. After training, the model can be used to generate new images with textual inversion
