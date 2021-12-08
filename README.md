# creating-ArtPorn-with-GANS

A simple DCGAN for creating artificial porn images.

![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
[![Python 3.9](https://img.shields.io/badge/python-3.9-blue.svg)](https://www.python.org/downloads/release/python-390/)
![Made with Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter)

## Why ArtPorn?
I used this term to describe the ambivalence of the here created images. Art in `ArtPorn` stands for *art* as well as for *artificial*, i.e. porn which was created by an artificial intelligence and which is abstract enough to be considered as art. 
So why porn and not other pictures? Well, why not ...? Of course GANs can create everything: faces, animals, plants, objects, etc. I was particular interested in wether the result will *activate* something in you, e.g. I find it interesting to constantly thinking what I see and if it might turn me on while studying the images.   
I didn't do any research about similar projects. I didn't do any picture pre-processing (also no )

## (First) Results
I scraped ca 10k images showing blowjobs and trained the network with 1000 epochs and almost 12h training time. Beside simple data augmentation no further image processing was implemented. This was the result:

![](/output/fake_porn_v1b.png)

## How does DCGANs work?
DCGAN stands for **D**eep **C**onvolutional **G**enerative **A**rtificial **N**etworks. A neural network type consisting of two networks: one network - the `Generator` - constantly creates random images and the other one  - the `Discriminator` - compares these *made-up* images with real images and tells the `Generator` how much to improve.

## How to use
1. Download images for the `Discriminator Network` either manually or by using the Web Crawler in [ScrapePornImages.ipynb](ScrapePornImages.ipynb).
2. Run the jupyter notebook [CreateArtPorn.ipynb](CreateArtPorn.ipynb) either locally (if you have GPU) or - like I did - on Google Colab. For the latter upload the images on Google Drive and mount it (see the code in the notebook).

## Whre to go next?
Preprocessing the images for the `Discriminator` - esp. selecting images which are more similar - will probably lead to more realistic results.

## Inspiration
- [DCGAN Tutorial](https://pytorch.org/tutorials/beginner/dcgan_faces_tutorial.html) by [@Nathan Inkawhich](https://github.com/inkawhich)
- [Generative Adversarial Networks (GANs) Specialization](https://www.deeplearning.ai/program/generative-adversarial-networks-gans-specialization/) by DeepLearning.AI