# SR_gan
  what is SR gan?
  
  Type of Generative Adversial Network(GAN) for Super resolution of image. For my SRgan code, it will return the image that has 4 times higher resolution than the input image.

# How it works
    
GAN

<img src="https://developers.google.com/static/machine-learning/gan/images/gan_diagram.svg" width = 800 height = 300>


1. GAN network has two models, Generator, Discriminator
2. Generator creates fake output based on the input
  2-1. Generator creates high resolution image based on the input image
3. Discriminator distinguish whether the generated images are fake or real
4. Based on the Discriminator's result and image comparison, the Generator and Discriminator tune themselves to reduce **loss**

    4-1. Loss function in this model will include BinaryCrossEntropy of whether Discriminator successfully classify real images as real or fake images as fake.
  
    4-2. The Code include **transfer learning** aspect in that the **loss** also include **MeanSquaredError** of VGG19 network
  
    - Transfer learning is utilizing network that is trained by other people. In this case, the code used VGG19 trained by imagenet dataset
    

5. As the two models go through the multiple epochs, the generator will make real-like fake image and the discriminator will have better ability to distinguish the fake and real images
      
      

# Result

         Input                            Output                            Original
![135](https://user-images.githubusercontent.com/111392592/188732402-570d26c5-e4c0-4534-a9da-187f7a738cc3.png)

![272 (1)](https://user-images.githubusercontent.com/111392592/188732410-3af51c6a-0110-4ccc-90d9-ca24f5fc5016.png)

![71](https://user-images.githubusercontent.com/111392592/188732415-b556ce20-11b9-42b6-9547-cf8720e38aca.png)


# Problem to solve

1. Should Improve Detail

  1-1. More epoch?
  
  1-2. More data?
  

2. Should be able to train large images

  2-1. Resource problem
  
    2-1-1. Hardware limit
   
 
# Reference

image
  https://developers.google.com/static/machine-learning/gan/images/gan_diagram.svg  (image for GAN)

Paper
  https://arxiv.org/pdf/1609.04802v5.pdf
  
Data
  https://www.image-net.org/download.php

  
      
