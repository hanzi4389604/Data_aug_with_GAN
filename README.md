# Augment the weather data to predict blackleg disease 
To enrich the small blackleg disease dataset (only 63 entries were collected in 2021), we selected the weighted form of the dynamic time warping barycentric averaging (DBA) technique (Petitjean et al., 2011; Petitjean et al., 2014; 2016) to augment the data. The results indicate that the augmented dataset did not improve AI performance. In current project, I try to use generative adversarial network (GAN) to augment the dataset. Traditionally, GAN was used in image augmentation, and the generated images can be easily evaluated through bare eyes. However, the weather data cannot be simply evaluated through human eyes. Thus, we used the MINST dataset to evaluate the network effectiveness, and then adjust the network to the blackleg weather data. Finally we use the generated weather data to train AI models in predicting the blackleg pandemic.

#Environment:

Python: 3.9.12

Cuda: 10.2

Pytorch: 1.12.1

jupyterlab: 3.3.2

# DCGAN
Train the weather data:

Original images looks like:

![Alt text](https://github.com/hanzi4389604/Data_aug_with_GAN/blob/master/Results/weather_syn0.png)

Synthesized images with 50 epoches training:

![Alt text](https://github.com/hanzi4389604/Data_aug_with_GAN/blob/master/Results/weather_syn1.png)


We tried the MINST dataset which have one channel:

Original images:

![Alt text](https://github.com/hanzi4389604/Data_aug_with_GAN/blob/master/Results/number_orig.png)

Synthesized images with 50 epoches training:

![Alt text](https://github.com/hanzi4389604/Data_aug_with_GAN/blob/master/Results/num_syn.png)

We also tried the CelebFaces dataset which have three channel:

Original images:

![Alt text](https://github.com/hanzi4389604/Data_aug_with_GAN/blob/master/Results/face_orig.png)

Synthesized images with 50 epoches training:

![Alt text](https://github.com/hanzi4389604/Data_aug_with_GAN/blob/master/Results/face_syn.png)


# I tried Cycle-GAN, but it might be not appropriate for the weather data. 

![Alt text](https://github.com/hanzi4389604/Data_aug_with_GAN/blob/master/final_zebra_horse.png)
