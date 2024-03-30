# Why LDM?
-  It applys noise diffusion on latent space instead of pixel space; therefore, it minimizes computing resource while retaining quality and flexibily of diffusion models
-  It accepts different controllable modality such as image, boundingbox, text
# How does it work?
# Model structure and key components:
<div align="center">
  <img src="https://github.com/CompVis/latent-diffusion/raw/main/assets/modelfigure.png" alt="Sublime's custom image"/>
</div>

- <div align="left"> Image conpression and depression: KL-regularized autoencoder was used as a **first_state_model** to encode images into latent features (encoder E) and decode latent features into image (decoder D). This autoencoder can be trained separatedly on different datasets, such as ImageNet, FFHQ, celebA-HQ, ADE20K, COCO-stuff, FaceHQ, and so on [2].</div>
- Latent space diffusion is an Unet model: It was train to predict noise embeded into the image at different scales???
- Condition embeding:
  - Concat
  - Attention
  - CrossAttention
- Speedup


# References
1. [High resolution image synthesis with latent diffusion models](https://arxiv.org/pdf/2112.10752.pdf)
2. [Taming-transformer](https://github.com/CompVis/taming-transformers)