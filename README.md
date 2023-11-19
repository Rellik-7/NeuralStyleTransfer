# NeuralStyleTransfer


Apply Neural Style Transfer to transform any photo or video into the artistic style of renowned paintings. This method allows for a single training session to produce an endless variety of images.
This approach is significantly faster than the optimization-based technique introduced by Gatys et al, commonly known as fast style transfer. The process involves training a feedforward network that applies artistic styles to images, utilizing the loss function outlined in Gatys et al's paper.
The feedforward network, functioning as a residual autoencoder, takes a content image as input and generates a stylized output. Additionally, the model incorporates instance normalization instead of batch normalization, as suggested in the paper titled "Instance Normalization: The Missing Ingredient for Fast Stylization."
Training is carried out using perceptual loss, as defined in the paper "Perceptual Losses for Real-Time Style Transfer and Super-Resolution." The Vgg19 model is employed to calculate perceptual loss, with further details provided in the associated paper.

# Usage Instructions

1.Run the following in project folder download requirements.
  ```sh
  pip install -r requirements.txt
  ```
2. Download the zipped images dataset from google drive <a href="https://drive.google.com/file/d/15IF18bDscAVg8eAta6PGtKYmLEta-Ofd/view?usp=sharing">link</a>.<br>
3. Run the jupyter notebook.



