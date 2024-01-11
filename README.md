# Variational Auto Encoders
This code implements a Variational Autoencoder (VAE) for generating and manipulating facial images using TensorFlow and Keras. Here's a brief description and definition of major concepts:

1. **Variational Autoencoder (VAE):**
   - A generative model that learns to encode and decode data.
   - Comprises an encoder that maps input data to a probability distribution in the latent space and a decoder that reconstructs the data from sampled points in this space.
   - Includes a sampling layer that introduces stochasticity, enabling generation of diverse samples.

2. **Encoder and Decoder:**
   - **Encoder:** Accepts input images and maps them to the latent space, producing mean and log-variance vectors.
   - **Decoder:** Reconstructs images from sampled points in the latent space.

3. **Sampling Layer:**
   - Introduced in the `Sampling` class, it samples from the learned distribution in the latent space during model training.

4. **Training the VAE:**
   - Trains the VAE using a custom loss function composed of a reconstruction loss and a KL divergence term.
   - The model is trained on a dataset of facial images to learn a representation in the latent space.

5. **Data Preprocessing:**
   - Images are loaded and preprocessed using TensorFlow's `image_dataset_from_directory` function.
   - Images are normalized to the range [0, 1] and converted to a float32 format.

6. **Callbacks:**
   - Utilizes various callbacks, such as model checkpointing and TensorBoard, for monitoring and saving the training progress.

7. **Image Generation:**
   - Generates images during training and saves them as checkpoints using the `ImageGenerator` callback.

8. **TensorBoard Logging:**
   - Logs training metrics and visualizations to TensorBoard for monitoring and analysis.

9. **Testing and Visualization:**
   - Samples images from the trained VAE and visualizes both real and reconstructed images.
   - Visualizes the latent space by sampling points and decoding them.

10. **Attribute Manipulation:**
   - Defines functions to extract an attribute vector for a specific facial attribute (e.g., Blond Hair).
   - Manipulates the latent space to emphasize or de-emphasize the chosen attribute.

11. **Facial Morphing:**
   - Illustrates facial morphing by interpolating between latent space representations of two images.

12. **Face Dataset and Labels:**
   - Uses the CelebA dataset, containing facial images of celebrities.
   - Labels such as hair color are utilized to perform attribute manipulation.

The code demonstrates the training and use of a VAE for generating realistic facial images and manipulating facial attributes in the latent space.
