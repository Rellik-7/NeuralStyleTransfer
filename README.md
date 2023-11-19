# NeuralStyleTransfer


Apply Neural Style Transfer to transform any photo or video into the artistic style of renowned paintings. This method allows for a single training session to produce an endless variety of images.
This approach is significantly faster than the optimization-based technique introduced by Gatys et al, commonly known as fast style transfer. The process involves training a feedforward network that applies artistic styles to images, utilizing the loss function outlined in Gatys et al's paper.
The feedforward network, functioning as a residual autoencoder, takes a content image as input and generates a stylized output. Additionally, the model incorporates instance normalization instead of batch normalization, as suggested in the paper titled "Instance Normalization: The Missing Ingredient for Fast Stylization."
Training is carried out using perceptual loss, as defined in the paper "Perceptual Losses for Real-Time Style Transfer and Super-Resolution." The Vgg19 model is employed to calculate perceptual loss, with further details provided in the associated paper.


![image](https://github.com/Rellik-7/NeuralStyleTransfer/assets/75270052/94799dbc-5ef9-40cf-89d0-9e238deaa0e9)
![image](https://github.com/Rellik-7/NeuralStyleTransfer/assets/75270052/6e565858-6174-4dda-939d-c7c09bbd84cb)


# Usage Instructions

1.Clone this repo and run the following in project folder to download requirements.
  ```sh
  pip install -r requirements.txt
  ```
2. Download the zipped images dataset from google drive <a href="https://drive.google.com/file/d/15IF18bDscAVg8eAta6PGtKYmLEta-Ofd/view?usp=sharing">link</a> in the same project folder.<br>
3. Run the jupyter notebook. A model checkpoint is provided in this repo for instant inference without training (nst_model_weights).


# Limitations

This approach involves training an autoencoder on 1 style image at a time. After the overhead of training, this approach is significantly faster than the approach by https://arxiv.org/abs/1508.06576 which involves directly training the image matrix. However that approach can accomodate different style images. My model can accomodate one for 1 set of encoder-decoder weights, making inference much faster but adaptability limited. 
Also, there might be high frequency artifacts in the generated images. Due to time constraits I was not able to completely remove them. Training on further epochs may solve this issue.

Note: For some reason the notebook view isnt displaying the inference results. They are added here.

# Content

![content](https://github.com/Rellik-7/NeuralStyleTransfer/assets/75270052/497b176a-c428-4cd1-b5cd-4524ff870746)

# Generated 

![style](https://github.com/Rellik-7/NeuralStyleTransfer/assets/75270052/f5b5321f-63d1-4cd9-99af-4ece231f23c7)


