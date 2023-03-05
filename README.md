# Watermark-Removal-From-Images
This repository contains the methodology utilized for the submission of the second problem statement for the Analytics Hackathon

The approach used is as follows,
- We performed watermark detection and drew contours and deleted these parts of the image.
- We then used deep-fill v2 pretrained model to fill these deleted images.

##Deepfill v2

DeepFill v2 is a state-of-the-art image inpainting model that uses deep learning techniques to complete missing or corrupted parts of an image. It is based on a generative adversarial network (GAN) architecture that consists of two neural networks: a generator and a discriminator.

The generator network takes as input an image with missing or corrupted parts and produces an output image that completes the missing regions. It consists of an encoder-decoder architecture with skip connections between corresponding encoder and decoder layers. The encoder part of the network extracts features from the input image, while the decoder part generates the output image using these features.

The generator network is trained using a combination of a reconstruction loss and an adversarial loss. The reconstruction loss measures the difference between the output image and the ground truth image, while the adversarial loss encourages the generator to produce output images that are indistinguishable from real images. The adversarial loss is computed using a discriminator network that tries to distinguish between the generated images and real images.

The discriminator network is trained to distinguish between real images and generated images produced by the generator network. It is also a convolutional neural network (CNN) that takes as input an image and produces a binary output that indicates whether the image is real or generated. The discriminator network is trained using a binary cross-entropy loss.

DeepFill v2 also incorporates a contextual attention module that helps the generator network to use contextual information from the surrounding image to fill in the missing regions. The contextual attention module uses a multi-scale approach to compute the attention map, which is used to guide the generator network to fill in the missing regions.

In addition, DeepFill v2 includes several other techniques such as a progressive training strategy, an adversarial loss with feature matching, and a spatially variant noise injection that help to improve the inpainting quality and speed.

Overall, DeepFill v2 is a powerful image inpainting model that can produce high-quality and visually plausible results even for complex images with large missing regions. Its architecture and training strategies are carefully designed to exploit the strengths of deep learning techniques for image inpainting.
