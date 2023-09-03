# satellite-2-maps

Location-based services significantly rely on accurate and up-to-date maps. Conventional map generation involves labor-intensive and time-consuming manual efforts, which restricts the map-update frequency leading to large delays in updating maps. In fast-developing cities and nations, quick updation of maps for a region manually is a tedious, and near to impossible task. Road works, detours and developments affect the region’s transportation routes and immediate and effective map updation is not only convenient for motorists but can also allow travelers to plan their journey better, ease congestion on roads and reduce overall travel time. In recent years, satellite images have become more ubiquitous, and converting them to map-style images has attracted attention. However, the underlying complexities and irregularities of road structures coupled with visually indistinguishable objects, obstructions, and poor weather conditions have made accurate and precise satellite-to-map conversions a challenging task.

## Generative Adversarial Networks (GANs)
GANs have been seen as a promising approach to this task. It is a dual-component model made up of a **generator** and a **discriminator**. They are a generative model that involves automatically learning and discovering information and useful patterns in the input data that can be used to generate valuable outputs. For this type of problem, we use “Image-to-Image Translation(I2I)” GANs that can help convert satellite-based images to identify features such as roads, buildings, water bodies, etc., and generate an image to represent it in a standard map format. The Pix2Pix GAN framework is a common framework for any image translation task. Hence, developing a deep learning model using GANs that can accurately generate maps can help automate the process and thus save time and resources.

### Conditional GAN (cGAN)
A specific type of GAN known as Conditional GAN or cGAN is an effective method for the purpose of accurate conversion of satellite images to map images. cGANs allow us to feed conditions or extra information such as labels to the generator and discriminator to learn the difference between them.
#### Proposed Generator model UNet3+:
- Reference: [UNet3+ Pytorch](https://github.com/avBuffer/UNet3plus_pth/tree/master/unet)
- accurately localizes objects but also produces coherent boundaries, even in small object circumstances
- full-scale skip connections and deep supervision are used

![UNet3+](https://www.mdpi.com/diagnostics/diagnostics-13-01624/article_deploy/html/images/diagnostics-13-01624-g009-550.jpg)
#### Discriminator model:
- Reference: [@anh-nn01](https://github.com/anh-nn01/Satellite-Imagery-to-Map-Translation-using-Pix2Pix-GAN-framework/tree/main)
- binary Convolutional Neural Network

## Dataset
- [Pix2Pix Maps (Kaggle), 1096 images](https://www.kaggle.com/datasets/alincijov/pix2pix-maps)
- 256x256 Satellite view image concatenated with 256x256 Map view image => 512x512 input data size  (each pixel in the satellite image represents the corresponding pixel as a map)


 


