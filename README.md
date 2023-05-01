# Replace Anything

## What is this?
This application can be used to edit specific parts of an image in two simple steps.

**Step 1**. Generate a mask using the Segment Anything Model ([SAM](https://github.com/facebookresearch/segment-anything#getting-started)) by Meta AI Research. SAM is able to accurately identify and isolate the specific areas of the image that you want to edit.

**Step 2**. Replace the specific parts of the image based on a text prompt using Diffusers library [inpaint pipeline](https://huggingface.co/docs/diffusers/main/en/api/pipelines/stable_diffusion/inpaint) by Hugging Face. This ensures smooth and seamless blending of the edited portions with the rest of the image, resulting in a natural and realistic final product.

This application is deployed and served using BentoML.

**Demo:**
![](https://github.com/yuqwu/Replace-Anything/blob/main/Demo1.gif)

## Getting Started
First download the trained model checkpoint [ViT-H SAM model](https://dl.fbaipublicfiles.com/segment_anything/sam_vit_h_4b8939.pth). 
```
wget https://dl.fbaipublicfiles.com/segment_anything/sam_vit_h_4b8939.pth
```

Before running the scripts, make sure you install the dependencies.
```
pip install -r requirements.txt
```

Use bentoml to serve the model.
```
bentoml serve
```

#
This project is intended for research purposes only and is not intended for commercial use or profit. This project is based on two open source models, Meta Segment Anything and Stable Diffusion, which are made available under the respective licenses.
